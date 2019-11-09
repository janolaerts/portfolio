<template>
  <div class="about">
    <div class="menu" @click="$router.push({ name: 'Nav' })"><img src="../assets/three-horizontal-lines.svg" width="30px" height="30px" alt="menu"></div>
    <div class="words-wrapper">
      <h1>Hello, I am Jan and I build</h1>
      <h1 :class="`words ${this.word}`">{{ word }}</h1>
    </div>
    <div class="technologies">
      <h1>I use <span>{{ technology }}</span></h1>
      <div class="logos">
        <img @mouseover="showTech('HTML')" height="32" width="32" src="../assets/html5.svg" />
        <img @mouseover="showTech('CSS')" height="32" width="32" src="../assets/css3.svg" />
        <img @mouseover="showTech('JavaScript')" height="32" width="32" src="../assets/javascript.svg" />
        <img @mouseover="showTech('React.js')" height="32" width="32" src="../assets/react.svg" />
        <img @mouseover="showTech('Vue.js')" height="32" width="32" src="../assets/vue-dot-js.svg" />
        <img @mouseover="showTech('Node.js')" height="32" width="32" src="../assets/node-dot-js.svg" />
        <img @mouseover="showTech('Firebase (db & auth)')" height="32" width="32" src="../assets/firebase.svg" />
        <img @mouseover="showTech('MongoDB')" height="32" width="32" src="../assets/mongodb.svg" />
      </div>
    </div>
    <div class="contact">
      <button @click="$router.push({ name: 'Contact' })">Contact me</button>
    </div>
      <img class="arrow" src="../assets/arrow.svg" alt="contact">
      <div @click="$router.push({ name: 'About' })" class="circle"><h1>J</h1></div>
  </div>
</template>

<script>
export default {
  name: 'About',
  data(){
    return {
     move: false,
     word: 'applications',
     words: ['applications', 'websites', 'market places', 'native apps'],
     index: 0,
     button: false,
     technology: null
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
    },
    showTech(technology){
      this.technology = technology
    }
  }
}
</script>

<style>
.about{
  background: black;
  position: absolute;
  height: 100%;
  width: 100%;
  top: 0;
  left: 0;
}
.about .menu{
  position: absolute;
  right: 2%;
  top: 2%;
  cursor: pointer;
  z-index: 1000;
}
.about .menu img{
  cursor: pointer;
}
.about .words-wrapper h1{
  position: relative;
  color: white;
  font-size: 50px;
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  margin: 0;
  top: 0px;
}
.about h1.applications{
  color: 	#cd6689;
}
.about h1.websites{
  color: #cd7766;
}
.about h1.market{
  color: #cd9166;
}
.about h1.native{
  color: #cd6677;
}
.about div .words{
  position: relative;
  
}
.about .technologies{
  position: absolute;
  width: 100%;
  height: 100px;
  bottom: 140px;
  border-top: 2px solid #cd6677;

}
.about .technologies h1{
  position: relative;
  font-size: 40px;
  text-align: center;
  color: white;
  bottom: 20px;
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
}
.about .technologies h1 span{
  color: #cd9166;
}
.about .technologies .logos{
  position: relative;
  display: grid;
  grid-template-columns: repeat(8, 1fr);
  bottom: 32.5px;
}
.about .technologies .logos img{
  margin: 0 auto;
}
.about .contact{
  position: absolute;
  display: inline-block;
  bottom: 80px;
  width: 100%;
  text-align: center;
}
.about .contact button{
  position: relative;
  border: 2px solid #cd6689;
  padding: 10px;
  color:#cd6689;
  width: 170px;
  font-weight: bold;
  background-color: rgba(255, 255, 255, 0);
  cursor: pointer;
}
.about .contact button:hover{
  border: 2px solid #cd6689;
  color: black;
  background: #cd6689;
}
.about .arrow{
  position: absolute;
  width: 20%;
  left: 40%;
  height: 50px;
  bottom: 1%;
  animation: idle 2s linear infinite alternate;
  animation-timing-function: ease;
}
.about .circle{
  position: fixed;
  width: 50px;
  height: 50px;
  bottom: 15px;
  left: 15px;
  border: 4px solid white;
  border-radius: 30px;
  cursor: pointer;
}
.about .circle h1{
  color: white;
  position: relative;
  text-align: center;
  top: -25%;
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
}
.about .circle:hover{
  animation: pop 1s linear;
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
@media all and (max-width: 991px){
  .about .words-wrapper h1{
    font-size: 40px;
  }
  .about .technologies h1{
    font-size: 35px;
  }
}

@media all and (max-width: 768px){
  .about .words-wrapper h1{
    font-size: 35px;
  }
  .about .technologies h1{
    font-size: 30px;
  }
}

@media all and (max-width: 575px){
  .about .words-wrapper h1{
    font-size: 30px;
  }
  .about .technologies h1{
    font-size: 25px;
  }
}

</style>