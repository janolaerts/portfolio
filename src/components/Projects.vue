<template>
  <div class="projects">
    <div @click="$router.push({ name: 'About' })" class="logo"><p>J</p></div>
    <div class="menu" @click="$router.push({ name: 'Nav' })"><img src="../assets/nav-icons/three-horizontal-lines-darker.svg" width="30px" height="30px" alt="menu"></div>
    <h1 class="my-projects">Projects</h1>
    <div class="projects-container">
      <div class="project1"><img width="400px" src="../assets/projects-photos/Jatha Psicopedagogia Laptop.png" alt="jatha psicopedagogia"></div>
      <div class="project1-info">
        <h1>Jatha Psicopedagogía</h1>
        <p class="intro">A website with a web shop</p>
        <p class="technologies">Made with <img width="32px" src="https://cdn.jsdelivr.net/npm/simple-icons@latest/icons/react.svg" alt="react"></p>
        <div class="buttons">
          <button class="website"><a href="https://jatha-psicopedagogia.web.app/" target="_blank">Visit website</a></button>
          <button><a href="https://github.com/janolaerts/jatha-psichopedagogia" target="_blank">Source code</a></button>
        </div>
      </div>
      <div class="project2"><img width="400px" src="../assets/projects-photos/Violeta Bazar Laptop.png" alt=""></div>
      <div class="project2-info">
        <h1>Violeta Bazar</h1>
        <p class="intro">An ecommerce store</p>
        <p class="technologies">Made with <img width="32px" src="https://cdn.jsdelivr.net/npm/simple-icons@latest/icons/node-dot-js.svg" alt="node"> and <img width="32px" src="https://cdn.jsdelivr.net/npm/simple-icons@latest/icons/mongodb.svg" alt="mongodb"> </p>
        <div class="buttons">
          <button class="website"><a href="https://violeta-bazar.herokuapp.com/" target="_blank">Visit website</a></button>
          <button><a href="https://github.com/janolaerts/Violeta-Bazar" target="_blank">Source code</a></button>
        </div>
      </div>
      <div class="project3"><img width="400px" src="../assets/projects-photos/Jatha Ventas Laptop.png" alt="jatha-ventas"></div>
      <div class="project3-info">
        <h1>Jatha Ventas</h1>
        <p class="intro">An application to keep track of your sold products</p>
        <p class="technologies">Made with <img width="32px" src="https://cdn.jsdelivr.net/npm/simple-icons@latest/icons/javascript.svg" alt="javascript"> and <img width="32px" src="https://cdn.jsdelivr.net/npm/simple-icons@latest/icons/firebase.svg" alt="firebase"></p>
        <div class="buttons">
          <button class="website"><a href="https://jatha-ventas.web.app/" target="_blank">Visit website</a></button>
          <button><a href="https://github.com/janolaerts/Jatha-Ventas" target="_blank">Source code</a></button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Projects',
  data(){
    return{

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
.projects .logo{
  position: fixed;
  color: black;
  border: 2px solid black;
  width: 50px;
  height: 50px;
  text-align: center;
  font-family:'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  top: 10px;
  left: 10px;
  font-size: 40px;
  cursor: pointer;
  z-index: 1001;
}
.projects .logo:hover{
  border-radius: 10px;
}
.projects .logo p{
  position: relative;
  text-align: center;
  cursor: pointer;
  margin: 0;
  top: 1px;
  z-index: 1002;
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
  background: rgba(255, 255, 255, 0.8);
  top: 10px;
}
.projects h1 span{
  position: relative;
  animation-timing-function: ease;
}
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
  overflow: hidden;
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
  animation: slideLeft 1s linear forwards;
  animation-timing-function: ease;
}
.projects-container .project2 img{
  position: relative;
  left: -200%;
  animation: slideLeft 1s .75s linear forwards;
  animation-timing-function: ease;
}
.projects-container .project3 img{
  position: relative;
  left: -200%;
  animation: slideLeft 1s 1.5s linear forwards;
  animation-timing-function: ease;
}
.projects-container .project1-info{
  flex-grow: 1;
  flex-basis: 400px;
  border-bottom: 2px solid #cd7766;
  position: relative;
  transform: rotateX(90deg);
  animation: flip .75s .25s linear forwards;
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
.projects-container .project2-info{
  flex-grow: 1;
  flex-basis: 400px;
  border-bottom: 2px solid #cd7766;
  transform: rotateX(90deg);
  animation: flip .75s 1s linear forwards;
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
.projects-container .project3-info{
  flex-grow: 1;
  flex-basis: 400px;
  transform: rotateX(90deg);
  animation: flip .75s 1.75s linear forwards;
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

.projects .projects-container a{
  text-decoration: none;
  color:navy;
}

.projects-container .buttons{
  display: grid;
  grid-gap: 10px;
  grid-template-columns: 1fr 1fr;
  width: 100%;
}
.projects-container button{
  padding: 10px 5px;
  font-family:'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  background: none;
  border: 2px solid #cd7766;
  cursor: pointer;
  width: 100px;
  position: relative;
  bottom: 2px;
}
.projects-container .buttons .website{
  position: relative;
  justify-self: end;
}
.projects-container button:hover{
  background: #cd7766;
}

/* responsive design */
@media all and (min-width: 991px){
  .projects-container{
    width: 1000px;
  }
}

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
  .projects .logo{
    width: 40px;
    height: 40px;
  }
  .projects .logo p{
    top: -3px;
  }
  .projects h1.my-projects{
    font-size: 35px;
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