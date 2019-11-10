<template>
<div class="page">
  <div class="menu-close" @click="$router.go(-1)"><img src="../assets/close-line.svg" width="30px" height="30px" alt="menu-close"></div>
  <div class="links">
    <div @click="$router.push({ name: 'About' })"><img src="../assets/menu.svg" width="40px" height="40px" alt="about"><h2 class="link-about">About me</h2></div>
    <div @click="$router.push({ name: 'Projects' })"><img src="../assets/code.svg" width="40px" height="40px" alt="project"><h2 class="link-my-projects">My projects</h2></div>
    <div @click="$router.push({ name: 'Resume' })"><img src="../assets/text-file-line.svg" width="40px" height="40px" alt="resume"><h2 class="link-resume">Resume</h2></div>
    <a href="https://github.com/janolaerts"><img src="../assets/github.svg" width="40px" height="40px" alt="github"><h2 class="link-github">Github</h2></a>
  </div>
  <div @click="$router.push({ name: 'About' })" class="circle"><h1>J</h1></div>
</div>
</template>

<script>
export default {
  name: 'Nav',
  data(){
    return {

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
  left: 60vw;
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
.links div:nth-child(3){
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
.links div:nth-child(3):hover{
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
  right: 40%;
  width: 150px;
  cursor: pointer;
  margin-top: 6px;
}
.circle{
  position: fixed;
  width: 50px;
  height: 50px;
  top: 15px;
  left: 15px;
  border: 4px solid white;
  border-radius: 30px;
  cursor: pointer;
}
.circle h1{
  color: white;
  position: relative;
  text-align: center;
  top: -25%;
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
}
.circle:hover{
  animation: pop 1s linear;
  animation-timing-function: ease;
}

/* animations */
@keyframes pop{
  0%{
    transform: scale(1);
  }
  50%{
    transform: scale(.9);
  }
  90%{
    transform: scale(1.1)
  }
  100%{
    transform: scale(1)
  }
}

/* responsive rules */
@keyframes menu{
  from{
    width: 0px
  }
  to{
    width: 210px
  }
}
</style>