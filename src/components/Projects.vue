<template>
  <div class="projects">
    <div class="menu" @click="$router.push({ name: 'Nav' })"><img src="../assets/nav-icons/three-horizontal-lines-darker.svg" width="30px" height="30px" alt="menu"></div>
    <h1 class="my-projects"><span>M</span><span>y</span><span>-</span><span>p</span><span>r</span><span>o</span><span>j</span><span>e</span><span>c</span><span>t</span><span>s</span></h1>
    <div class="projects-container">
      <div class="project1"><img width="400px" src="../assets/projects-photos/Jatha Ventas Laptop.png" alt="jatha-ventas"></div>
      <div class="project1-info">
        <h1>Jatha Ventas</h1>
        <p class="intro">An application to keep track of your sold products</p>
        <p class="technologies">Made with <img width="32px" src="https://cdn.jsdelivr.net/npm/simple-icons@latest/icons/javascript.svg" alt="javascript"> and <img width="32px" src="https://cdn.jsdelivr.net/npm/simple-icons@latest/icons/firebase.svg" alt="firebase"></p>
        <div class="buttons">
          <button class="website"> <a href="https://jatha-ventas.web.app/" target="_blank">Visit website</a></button>
          <button><a href="https://github.com/janolaerts/Jatha-Ventas" target="_blank">Source code</a></button>
        </div>
      </div>
      <div class="project2"><img width="400px" src="../assets/projects-photos/Taco App Laptop.png" alt="taco-app"></div>
      <div class="project2-info">
        <h1>Taco App</h1>
        <p class="intro">A mockup of an order application</p>
        <p class="technologies">Made with <img width="32px" src="https://cdn.jsdelivr.net/npm/simple-icons@latest/icons/react.svg" alt="react"></p>
        <div class="buttons">
          <button class="website"><a href="https://taco-app-ad29b.web.app/" target="_blank">Visit website</a></button>
          <button><a href="https://github.com/janolaerts/Taco-App" target="_blank">Source code</a></button>
        </div>
      </div>
      <div class="project3"><img width="400px" src="../assets/projects-photos/Askbot Laptop.png" alt=""></div>
      <div class="project3-info">
        <h1>Askbot</h1>
        <p class="intro">An API which allows to upload and ask questions</p>
        <p class="technologies">Made with <img width="32px" src="https://cdn.jsdelivr.net/npm/simple-icons@latest/icons/node-dot-js.svg" alt="node"> and <img width="32px" src="https://cdn.jsdelivr.net/npm/simple-icons@latest/icons/mongodb.svg" alt="mongodb"> </p>
        <button><a href="https://github.com/janolaerts/Askbot" target="_blank">Source code</a></button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Projects',
  data(){
    return{
      wiggle: false
    }
  }
}
</script>

<style>
.projects{
  background: white;
  width: 100%;
  height: fit-content;
  position: absolute;
  top: 0;
  left: 0;
}
.projects .menu{
  position: fixed;
  right: 2%;
  top: 2%;
  cursor: pointer;
  z-index: 1010;
}
.projects h1.my-projects{
  position: fixed;
  color: black;
  font-size: 50px;
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  text-align: center;
  z-index: 1000;
  width: 100%;
  margin: 0;
  background: rgba(255, 255, 255, 1);
}
.projects h1 span{
  position: relative;
  animation-timing-function: ease;
}
/*.projects h1 span:nth-child(1){
  animation: slideLeft 1.5s linear forwards;
}
.projects h1 span:nth-child(2){
  animation: slideLeft 1.4s linear forwards;
}
.projects h1 span:nth-child(3){
  visibility: hidden;
  animation: slideLeft 1.3s linear forwards;
}
.projects h1 span:nth-child(4){
  animation: slideLeft 1.2s linear forwards;
}
.projects h1 span:nth-child(5){
  animation: slideLeft 1.1s linear forwards;
}
.projects h1 span:nth-child(6){
  animation: slideLeft 1s linear forwards;
}
.projects h1 span:nth-child(7){
  animation: slideLeft .9s linear forwards;
}
.projects h1 span:nth-child(8){
  animation: slideLeft .8s linear forwards;
}
.projects h1 span:nth-child(9){
  animation: slideLeft .7s linear forwards;
}
.projects h1 span:nth-child(10){
  animation: slideLeft .6s linear forwards;
}
.projects h1 span:nth-child(11){
  animation: slideLeft .5s linear forwards;
}*/
.projects-container{
  position: relative;
  background: white;
  top: 75px;
  width: 70%;
  margin: 0 auto;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  border-radius: 10px;
}
.projects-container h1{
  color: #cd7766;
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  font-size: 25px;
  position: relative;
  text-align: center;
}
.projects-container .project1 img{
  position: relative;
  left: -200%;
  animation: slideLeft 1s .75s linear forwards;
  animation-timing-function: ease;
}
.projects-container .project2 img{
  position: relative;
  left: -200%;
  animation: slideLeft 1s 1.5s linear forwards;
  animation-timing-function: ease;
}
.projects-container .project3 img{
  position: relative;
  left: -200%;
  animation: slideLeft 1s 2.25s linear forwards;
  animation-timing-function: ease;
}
.projects-container .project1-info{
  flex-grow: 1;
  flex-basis: 400px;
  border-bottom: 2px solid #cd7766;
  position: relative;
  transform: rotateX(90deg);
  animation: flip .75s 1s linear forwards;
  animation-timing-function: ease;
}
.projects-container .project1-info .intro{
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  font-size: 20px;
}
.projects-container .project1-info .technologies{
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  font-size: 20px;
  position: relative;
  top: -5px;
}
.projects-container .project1-info .buttons{
  display: grid;
  grid-gap: 10px;
  grid-template-columns: 1fr 1fr;
  width: 100%;
}
.projects-container .project1-info button{
  padding: 10px 5px;
  font-family:'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  background: none;
  border: 2px solid #cd7766;
  cursor: pointer;
  width: 100px;
  position: relative;
  bottom: 2px;
}
.projects-container .project1-info button:hover{
  background: #cd7766;
}
.projects-container .project1-info .buttons .website{
  position: relative;
  justify-self:end;
}
.projects-container .project2-info{
  flex-grow: 1;
  flex-basis: 400px;
  border-bottom: 2px solid #cd7766;
  transform: rotateX(90deg);
  animation: flip .75s 1.75s linear forwards;
  animation-timing-function: ease;
}
.projects-container .project2-info .intro{
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  font-size: 20px;
}
.projects-container .project2-info .technologies{
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  font-size: 20px;
  position: relative;
  top: -5px;
}
.projects-container .project2-info .buttons{
  display: grid;
  grid-gap: 10px;
  grid-template-columns: 1fr 1fr;
  width: 100%;
}
.projects-container .project2-info button{
  padding: 10px 5px;
  font-family:'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  background: none;
  border: 2px solid #cd7766;
  cursor: pointer;
  width: 100px;
  position: relative;
  bottom: 2px;
}
.projects-container .project2-info .buttons .website{
  position: relative;
  justify-self: end;
}
.projects-container .project2-info button:hover{
  background: #cd7766;
}
.projects-container .project3-info{
  flex-grow: 1;
  flex-basis: 400px;
  transform: rotateX(90deg);
  animation: flip .75s 2.5s linear forwards;
  animation-timing-function: ease;
}
.projects-container .project3-info .intro{
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  font-size: 20px;
}
.projects-container .project3-info .technologies{
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  font-size: 20px;
  position: relative;
  top: -5px;
}
.projects-container .project3-info button{
  padding: 10px 10px;
  font-family:'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  background: none;
  border: 2px solid #cd7766;
  cursor: pointer;
  margin-bottom: 5px;
  display: block;
  margin: 0 auto 5px auto;
  position: relative;
  bottom: 3px;
}
.projects-container .project3-info button:hover{
  background: #cd7766;
}
.projects .projects-container a{
  text-decoration: none;
  color:navy;
}

/* responsive design */
@media all and (max-width: 991px){
  .projects h1.my-projects{
    font-size: 40px;
  }
}

@media all and (max-width: 768px){
  .projects h1.my-projects{
    font-size: 40px;
  }
}

@media all and (max-width: 575px){
  .projects h1.my-projects{
    font-size: 30px;
  }
  .projects-container .project1 img{
    width: 300px;
  }
  .projects-container .project2 img{
    width: 300px;
  }
  .projects-container .project3 img{
    width: 300px;
  }
}

/* animations */
@keyframes slideLeft{
  from{
    left: -200%;
  }
  to{
    left: 0%;
  }
}

@keyframes flip{
  from{
    transform: rotateX(90deg);
  }
  to{
    transform: rotateX(0deg);
  }
}
</style>