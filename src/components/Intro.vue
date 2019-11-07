<template>
  <div class="intro">
    <div>
      <h1>Hello, I am Jan and I build</h1>
      <h1 :class="`words ${this.word}`">{{ word }}</h1>
    </div>
    <div class="links">
      <div><img src="../assets/code.svg" alt="project"></div>
      <div><img src="../assets/text-file-line.svg" alt="resume"></div>
      <div><img src="../assets/github.svg" alt="github"></div>
    </div>
    <div class="contact">
      <button @click="$router.push({ name: 'Contact' })">Contact me</button>
    </div>
      <img class="arrow" src="../assets/arrow.svg" alt="menu">
  </div>
</template>

<script>
export default {
  name: 'Intro',
  data(){
    return {
     move: false,
     word: 'applications',
     words: ['applications', 'websites', 'market places', 'native apps'],
     index: 0,
     button: false
    }
  },
  created(){
    setInterval(() => {
     this.changeWord()
    }, 2000)
  },
  methods: {
    changeWord(){
      this.word = this.words[this.index]
      this.index++
      if(this.index >= 4){
        this.index = 0
      }
    }
  }
}
</script>

<style>
.intro{
  background: mediumaquamarine;
  position: absolute;
  height: 100%;
  width: 100%;
  top: 0;
  left: 0;
}
.intro h1{
  position: relative;
  color: white;
  font-size: 300%;
  padding: 0px 20px;
  top: 100px;
  font-size: 50px;
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  margin: 0;
}
.intro h1.applications{
  color: 	#cd6689;
}
.intro h1.websites{
  color: #cd7766;
}
.intro h1.market{
  color: #cd9166;
}
.intro h1.native{
  color: #cd6677;
}
.intro div .words{
  position: relative;
  left: 0px;
}
.intro .links{
  position: absolute;
  height: 25%;
  width: 45px;
  bottom: 30%;
  right: 10px;

}
.intro .links div{
  position: absolute;
  background: white;
  width: 0px;
  height: 40px;
  right: 2%;
}
.intro .links img{
  position: absolute;
  width: 40px;
  height: 40px;
  cursor: pointer;
  right: 2%;
}
.intro .links :nth-child(1){
  margin-top: 0px;
  animation: fall1 2s linear;
  animation-timing-function: ease;
}
.intro .links :nth-child(2){
  margin: 75px 0;
  animation: fall2 1.5s linear;
  animation-timing-function: ease;
}
.intro .links :nth-child(3){
  margin: 150px 0;
  animation: fall3 1s linear;
  animation-timing-function: ease;
}
.intro .links div:nth-child(1):hover{
  background: white;
  right: 0%;
  animation: menu1 1s linear forwards;
  animation-timing-function: ease;
}
.intro .links div:nth-child(2):hover{
  background: white;
  right: 0%;
  animation: menu1 1s linear forwards;
  animation-timing-function: ease;
}
.intro .links div:nth-child(3):hover{
  background: white;
  right: 0%;
  animation: menu1 1s linear forwards;
  animation-timing-function: ease;
}
.intro .contact{
  position: absolute;
  display: inline-block;
  bottom: 90px;
  width: 100%;
  text-align: center;
}
.intro .contact button{
  position: relative;
  border: 2px solid navy;
  padding: 10px;
  color:navy;
  width: 170px;
  font-weight: bold;
  background-color: rgba(255, 255, 255, 0);
  cursor: pointer;
}
.intro .contact button:hover{
  border: 2px solid navy;
  color: mediumaquamarine;
  background: navy;
}
.intro .arrow{
  position: absolute;
  width: 20%;
  left: 40%;
  height: 50px;
  bottom: 1%;
  animation: idle 2s linear infinite alternate;
  animation-timing-function: ease;
}

/* animations */
@keyframes idle{
  from{
    transform: translateY(0px);
  }
  to{
    transform: translateY(-15px);
  }
}
@keyframes fall1{
  from{
    top: -300%
  }
  to{
    top: 0%
  }
}
@keyframes fall2{
  from{
    top: -300%
  }
  to{
    top: 0%
  }
}
@keyframes fall3{
  from{
    top: -300%
  }
  to{
    top: 0%
  }
}
@keyframes menu1{
  from{
    width: 0px
  }
  to{
    width: 250px
  }
}
@keyframes menu2{
  from{
    width: 0px
  }
  to{
    width: 250px
  }
}
@keyframes menu3{
  from{
    width: 0px
  }
  to{
    width: 250px
  }
}

</style>