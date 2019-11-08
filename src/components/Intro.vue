<template>
  <div class="intro">
    <div>
      <h1>Hello, I am Jan and I build</h1>
      <h1 :class="`words ${this.word}`">{{ word }}</h1>
    </div>
    <div class="technologies">
      <h1>I use <span>{{ technology }}</span></h1>
      <div class="logos">
        <img @mouseover="showTech('HTML')" height="32" width="32" src="https://cdn.jsdelivr.net/npm/simple-icons@latest/icons/html5.svg" />
        <img @mouseover="showTech('CSS')" height="32" width="32" src="https://cdn.jsdelivr.net/npm/simple-icons@latest/icons/css3.svg" />
        <img @mouseover="showTech('JavaScript')" height="32" width="32" src="https://cdn.jsdelivr.net/npm/simple-icons@latest/icons/javascript.svg" />
        <img @mouseover="showTech('React')" height="32" width="32" src="https://cdn.jsdelivr.net/npm/simple-icons@latest/icons/react.svg" />
        <img @mouseover="showTech('Node.js')" height="32" width="32" src="https://cdn.jsdelivr.net/npm/simple-icons@latest/icons/node-dot-js.svg" />
        <img @mouseover="showTech('Vue.js')" height="32" width="32" src="https://cdn.jsdelivr.net/npm/simple-icons@latest/icons/vue-dot-js.svg" />
        <img @mouseover="showTech('Firebase (db & auth)')" height="32" width="32" src="https://cdn.jsdelivr.net/npm/simple-icons@latest/icons/firebase.svg" />
        <img @mouseover="showTech('MongoDB')" height="32" width="32" src="https://cdn.jsdelivr.net/npm/simple-icons@latest/icons/mongodb.svg" />
      </div>
    </div>
    <div class="links">
      <div @click="$router.push({ name: 'Projects' })"><img src="../assets/code.svg" alt="project"><h2 class="link-my-projects">My projects</h2></div>
      <div @click="$router.push({ name: 'Resume' })"><img src="../assets/text-file-line.svg" alt="resume"><h2 class="link-resume">Resume</h2></div>
      <a href="https://github.com/janolaerts"><img src="../assets/github.svg" alt="github"><h2 class="link-github">Github</h2></a>
    </div>
    <div class="contact">
      <button @click="$router.push({ name: 'Contact' })">Contact me</button>
    </div>
      <img class="arrow" src="../assets/arrow.svg" alt="contact">
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
     button: false,
     technologies: ['HTML', 'CSS', 'JavaScript', 'React', 'Node.js', 'Vue.js', 'Firebase (db & auth)', 'MongoDB'],
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
  padding: 0px 20px;
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
.intro .technologies{
  position: absolute;
  width: 100%;
  height: 100px;
  bottom: 140px;
  border-top: 2px solid #cd6677;
  border-bottom: 2px solid #cd6677;
}
.intro .technologies h1{
  position: relative;
  font-size: 40px;
  text-align: center;
}
.intro .technologies .logos{
  position: relative;
  display: grid;
  grid-template-columns: repeat(8, 1fr);
  top: 20%;
}
.intro .technologies .logos img{
  margin: 0 auto;
}
.intro .links{
  position: absolute;
  height: 25%;
  width: 45px;
  bottom: 300px;
  right: 10px;
}
.intro .links div, .intro .links a{
  position: absolute;
  background: white;
  width: 0px;
  height: 40px;
  right: 2%;
}
.intro .links img, .intro .links a img{
  position: absolute;
  width: 40px;
  height: 40px;
  cursor: pointer;
  right: 6%;
}
.intro .links div:nth-child(1){
  margin-top: 0px;
}
.intro .links div:nth-child(2){
  margin: 75px 0;
}
.intro .links a{
  margin: 150px 0;
}
.intro .links div:nth-child(1):hover{
  background: #cd6689;
  right: 0%;
  animation: menu1 1s linear forwards;
  animation-timing-function: ease;
}
.intro .links div:nth-child(2):hover{
  background: #cd7766;
  right: 0%;
  animation: menu1 1s linear forwards;
  animation-timing-function: ease;
}
.intro .links a:hover{
  background: #cd9166;
  right: 0%;
  animation: menu1 1s linear forwards;
  animation-timing-function: ease;
}
.intro .links h2{
  color: whitesmoke;
  position: fixed;
  right: 60px;
  width: 150px;
  cursor: pointer;
  margin-top: 6px;
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

@keyframes menu1{
  from{
    width: 0px
  }
  to{
    width: 210px
  }
}
@keyframes menu2{
  from{
    width: 0px
  }
  to{
    width: 210px
  }
}
@keyframes menu3{
  from{
    width: 0px
  }
  to{
    width: 210px
  }
}

/* responsive rules */
@media all and (max-width: 991px){
  .intro h1{
    font-size: 40px;
  }
  .intro .technologies h1{
    font-size: 35px;
  }
}

@media all and (max-width: 768px){
  .intro h1{
    font-size: 35px;
  }
  .intro .technologies h1{
    font-size: 30px;
  }
}

@media all and (max-width: 575px){
  .intro h1{
    font-size: 30px;
  }
  .intro .technologies h1{
    font-size: 25px;
  }
}

</style>