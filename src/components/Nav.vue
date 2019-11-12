<template>
<div class="page">
  <div class="menu-close" @click="$router.go(-1)"><img src="../assets/nav-icons/close-line.svg" width="30px" height="30px" alt="menu-close"></div>
  <div class="links">
    <div @click="$router.push({ name: 'About' })"><img src="../assets/nav-icons/menu.svg" width="40px" height="40px" alt="about"><h2 class="link-about">About me</h2></div>
    <div @click="$router.push({ name: 'Projects' })"><img src="../assets/nav-icons/code.svg" width="40px" height="40px" alt="project"><h2 class="link-my-projects">My projects</h2></div>
    <a @click="downloadPDF"><img src="../assets/nav-icons/text-file-line.svg" width="40px" height="40px" alt="resume"><h2 class="link-resume">Resume</h2></a>
    <a href="https://github.com/janolaerts" target="_blank"><img src="../assets/nav-icons/github.svg" width="40px" height="40px" alt="github"><h2 class="link-github">Github</h2></a>
  </div>
</div>
</template>

<script>
import axios from 'axios'

export default {
  name: 'Nav',
  data(){
    return {
  
    }
  },
  methods: {
    downloadPDF(){
      axios({
        method: 'GET',
        url: 'Resume.pdf',
        responseType: 'blob'
      })
      .then(response => {
        let fileURL = window.URL.createObjectURL(new Blob ([response.data], { type: 'application/pdf' }))
        let fileLink = document.createElement('a')

        fileLink.href = fileURL
        fileLink.setAttribute('download', 'Resume Jan Olaerts.pdf')
        document.body.appendChild(fileLink)
        
        fileLink.click()
      })
      .catch(error => console.log(error))
    }
  }
}
</script>

<style>
.page{
  background: black;
  position: absolute;
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
}
.page .menu-close{
  position: absolute;
  right: 2%;
  top: 2%;
  cursor: pointer;
  z-index: 1000;
}
.links{
  position: absolute;
  height: 25%;
  width: 45px;
  top: 35%;
  /*left: 60vw;*/
  right: 2%;
}
.links div, .links a{
  position: absolute;
  background: white;
  width: 0px;
  height: 40px;
  right: 2%;
}
.links img, .links a img{
  position: absolute;
  width: 40px;
  height: 40px;
  cursor: pointer;
  right: 6%;
}
.links div:nth-child(1){
  margin-top: 0px;
}
.links div:nth-child(2){
  margin: 75px 0;
}
.links a:nth-child(3){
  margin: 150px 0;
}
.links a{
  margin: 225px 0;
}
.links div:nth-child(1):hover{
  background: #cd6689;
  right: 0%;
  animation: menu 1s linear forwards;
  animation-timing-function: ease;
}
.links div:nth-child(2):hover{
  background: #cd7766;
  right: 0%;
  animation: menu 1s linear forwards;
  animation-timing-function: ease;
}
.links a:nth-child(3):hover{
  background: tomato;
  right: 0%;
  animation: menu 1s linear forwards;
  animation-timing-function: ease;
}
.links a:hover{
  background: #cd9166;
  right: 0%;
  animation: menu 1s linear forwards;
  animation-timing-function: ease;
}
.links h2{
  color: whitesmoke;
  position: fixed;
  right: 80px;
  width: 150px;
  cursor: pointer;
  margin-top: 6px;
}

/* responsive rules */
@media all and (max-width: 1300px){
  .links h2{
    right: 60px;
  }
}

@media all and (max-width: 768px){

}

@media all and (max-width: 575px){

  .links{
    right: 2%;
  }
  .links h2{
    right: 50px;
  }
}

/* animations */

@keyframes menu{
  from{
    width: 0px
  }
  to{
    width: 210px
  }
}
</style>