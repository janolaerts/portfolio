<template>
  <div class="resume">
    <div class="menu" @click="$router.push({ name: 'Nav' })"><img src="../assets/three-horizontal-lines-darker.svg" width="30px" height="30px" alt="menu"></div>
    <h1>Resume</h1>
  </div>
</template>

<script>
export default {
  name: 'Resume',
  data(){
    return{

    }
  }
}
</script>

<style>
.resume .menu{
  position: fixed;
  right: 2%;
  top: 2%;
  cursor: pointer;
  z-index: 1010;
}
.resume h1{
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

/* responsive design */
@media all and (max-width: 991px){
  .resume h1{
    font-size: 40px;
  }
}

@media all and (max-width: 768px){
  .resume h1{
    font-size: 40px;
  }
}

@media all and (max-width: 575px){
  .resume h1{
    font-size: 30px;
  }
}
</style>