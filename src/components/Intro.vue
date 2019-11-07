<template>
  <div class="intro">
    <div class="flags">
      <img class="peru" @click="setLan('peru')" :class="{ selected: spanish }" src="../assets/pe.svg" width="70px" alt="peru">
      <img class="uk" @click="setLan('uk')" :class="{ selected: !spanish }" src="../assets/gb.svg" width="70px" alt="united-kingdom">
    </div>
    <h1 v-if="!spanish">Hello, I am Jan and I like building applications and websites</h1>
    <h1 v-if="spanish">Buenos días, yo soy Jan y me gusta hacer aplicaciones y páginas web</h1>
    <img class="menu" :class="{ move :move }" src="../assets/menu.svg" width="20vw" alt="menu">
  </div>
</template>

<script>
export default {
  name: 'Intro',
  data(){
    return {
     spanish: false,
     move: false
    }
  },
  created(){
    this.move = true
  },
  methods: {
    setLan(country){
      country === 'peru' ? this.spanish = true : this.spanish = false
    }
  }
}
</script>

<style>
.intro{
  position: absolute;
  height: 100%;
  width: 100%;
  top: 0;
  left: 0;
  background: black;
}
.intro .flags{
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-gap: 20px;
  width: 10%;
  height: 60px;
  margin-top: 20px;
  margin-left: 20px;
}
.intro .flags img{
  cursor: pointer;
  border-radius: 10%;
  opacity: .5;
}
.intro .flags img:hover{
  opacity: 1;
  transform: scale(1.2);
}
.intro .flags img.selected{
  opacity: 1;
}
.intro h1{
  position: relative;
  text-align: center;
  color: white;
  font-size: 300%;
  padding: 0px 20px;
  top: 25%;
}
.intro .menu{
  position: absolute;
  left: 50%;
  width: 25px;
  height: 50px;
  bottom: 1%;
  transform: rotateZ(-90deg);
  cursor: pointer;
}
.intro .menu:hover{
  transform: rotateZ(270deg);
}
</style>