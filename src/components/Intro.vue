<template>
  <div class="intro">
    <img src="../assets/menu.svg" width="40vw" alt="menu">
    <h1><b>J</b><small>an</small></h1>
  </div>
</template>

<script>
export default {
  name: 'Intro',
  data(){
    return {

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
  background: #1d0d6e;
}
.intro h1{
  position: relative;
  text-align: center;
  height: 25%;
  top: 12.5%;
  color: white;
  font-size: 1700%;
}
.intro h1 small{
  color: grey;
}
.intro img{
  position: absolute;
  left: 1.5%;
  height: 10%;
  top:42.5%;
  cursor: pointer;
}
</style>