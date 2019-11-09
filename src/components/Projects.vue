<template>
  <div class="projects">
    <div class="menu" @click="$router.push({ name: 'Nav' })"><img src="../assets/three-horizontal-lines-darker.svg" width="30px" height="30px" alt="menu"></div>
    <h1><span>M</span><span>y</span><span>-</span><span>p</span><span>r</span><span>o</span><span>j</span><span>e</span><span>c</span><span>t</span><span>s</span></h1>
    <div class="flex-container">
      <div class="project1">
        <h2>Jatha Ventas</h2>
      </div>
      <div class="project2">
        <h2>Taco App</h2>
      </div>
      <div class="project3">
        <h2>Askbot</h2>
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
.projects .menu{
  position: fixed;
  right: 2%;
  top: 2%;
  cursor: pointer;
  z-index: 1010;
}
.projects{
  background: #cd9166;
  width: 100%;
  height: 100%;
  position: absolute;
  top: 0;
  left: 0;
}
.projects h1{
  position: fixed;
  color: #cd6677;
  font-size: 300%;
  padding: 20px;
  font-size: 50px;
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  margin: 0;
  padding: 0px 0px 0px 2.5%;
  z-index: 1000;
  background: rgba(205, 145, 102, .5);
  width: 100%;
}
.projects h1 span{
  position: relative;
  animation-timing-function: ease;
}
.projects h1 span:nth-child(1){
  animation: slide 1.5s linear forwards;
}
.projects h1 span:nth-child(2){
  animation: slide 1.4s linear forwards;
}
.projects h1 span:nth-child(3){
  visibility: hidden;
  animation: slide 1.3s linear forwards;
}
.projects h1 span:nth-child(4){
  animation: slide 1.2s linear forwards;
}
.projects h1 span:nth-child(5){
  animation: slide 1.1s linear forwards;
}
.projects h1 span:nth-child(6){
  animation: slide 1s linear forwards;
}
.projects h1 span:nth-child(7){
  animation: slide .9s linear forwards;
}
.projects h1 span:nth-child(8){
  animation: slide .8s linear forwards;
}
.projects h1 span:nth-child(9){
  animation: slide .7s linear forwards;
}
.projects h1 span:nth-child(10){
  animation: slide .6s linear forwards;
}
.projects h1 span:nth-child(11){
  animation: slide .5s linear forwards;
}
.flex-container{
  position: relative;
  top: 75px;
  width: 95%;
  height: 650px;
  margin: 0 auto;
  display: flex;
  flex-wrap: wrap;
  padding: 5px;
}
.flex-container .project1{
  background: url('../assets/jatha-ventas.png') no-repeat top;
  background-size:cover;
  flex-basis: 450px;
  flex-grow: 1;
  margin: 5px;
  border-radius: 10px;
}
.flex-container .project2{
  background: url('../assets/taco-app.png') no-repeat top;
  background-size: cover;
  flex-basis: 450px;
  flex-grow: 1;
  margin: 5px;
  border-radius: 10px;
}
.flex-container .project3{
  background: url('../assets/askbot.png') no-repeat top;
  background-size: cover;
  flex-basis: 450px;
  flex-grow: 1;
  margin: 5px;
  border-radius: 10px;
}

/* animations */
@keyframes slide{
  from{
    left: -300px;
  }
  to{
    left: 0px;
  }
}
@keyframes wiggle{
  0%{
    left: -10px;
  }
  25%{
    left: 10px;
  }
  50%{
    left: -5px;
  }
  75%{
    left: 5px;
  }
  100%{
    left: 0px;
  }
}
</style>