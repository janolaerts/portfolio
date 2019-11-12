<template>
  <div class="contact">
    <div @click="$router.push({ name: 'About' })" class="logo"><p>J</p></div>
    <div class="menu" @click="$router.push({ name: 'Nav' })"><img src="../assets/nav-icons/three-horizontal-lines.svg" width="30px" height="30px" alt="menu"></div>
    <h1>Contact</h1>
    <form @submit.prevent="submitForm">
      <input type="text" name="user_name" v-model="name" placeholder="Please enter your full name">
      <input type="text" name="user_email" v-model="email" placeholder="Please enter your email">
      <input type="textarea" name="message" v-model="message" placeholder="What do you want to ask?">
      <button type="submit" value="Send">Submit</button>
      <div class="feedback">{{ feedback }}</div>
    </form>
  </div>
</template>

<script>
import emailjs from 'emailjs-com'

export default {
  name: 'Contact',
  data(){
    return{
      name: null,
      email: null,
      message: null,
      feedback: null
    }
  },
  methods: {
    submitForm(){
      if(this.name && this.email && this.message){
        this.verifyEmail()
      }
      else{
        this.feedback = 'Please fill in all the fields'
      }
    },
    verifyEmail(){
      const emailRegEx = /^([a-z\d.-]+)@([a-z\d-]+)\.([a-z]{2,8})(\.[a-z]{2,8})?$/
      if(emailRegEx.test(this.email)){
        this.sendEmail()
        this.name = null
        this.email = null
        this.message = null
        this.feedback = 'Thank you for contacting, I will respond as soon as possible'
      }
      else{
        this.feedback = 'Please fill in a valid email'
      }
    },
    sendEmail(){
      emailjs.send('gmail', 'email', { "user_name": this.name, "user_email": this.email, "message": `${this.message} This message is from ${this.name} with email: ${this.email}` }, 'user_4uQ2Gl25NDESShekYLk8G')
      .then(response => console.log(response.status, response.text))
      .catch(error => console.log(error))
    },
  }
}
</script>

<style>
.contact .menu{
  position: absolute;
  right: 2%;
  top: 2%;
  cursor: pointer;
  z-index: 1000;
}
.contact .logo{
  position: fixed;
  color: black;
  border: 2px solid white;
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
/*.contact .logo:hover{
  animation: rotate .75s linear forwards;
  animation-timing-function: ease;
}*/
.contact .logo p{
  position: relative;
  text-align: center;
  cursor: pointer;
  margin: 0;
  top: 1px;
  z-index: 1002;
  color: white;
}
.contact{
  position: absolute;
  width: 100%;
  height: 100%;
  top: 0%;
  left: 0%;
  background: black;
}
.contact h1{
  display: block;
  text-align: center;
  font-size: 50px;
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  color: mediumaquamarine;
  margin: 0;
  position: relative;
  top: 10px;
}
.contact .name{
  color: white;
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  position: absolute;
  left: 50%;
}
.contact form{
  position: relative;
  margin: 0 auto;
  height: 50%;
  width: 50%;
  text-align: center;
  border-radius: 10px;
  top: 40px;
}
.contact form input{
  width: 90%;
  height: 30px;
  margin-top: 10px;
  border: none;
  border-bottom: 1px solid white;
  border: 0px 0px 2px 0px;
  background: none;
  color: mediumaquamarine;
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  font-size: 20px;
}
.contact form input:nth-child(1){
  transform: rotateY(90deg);
  animation: skew .75s linear forwards;
  animation-timing-function: ease;
}
.contact form input:nth-child(2){
  transform: rotateY(90deg);
  animation: skew .75s .2s linear forwards;
  animation-timing-function: ease;
}
.contact form input:nth-child(3){
  transform: rotateY(90deg);
  animation: skew .75s .4s linear forwards;
  animation-timing-function: ease;
}
.contact form button{
  width: 25%;
  margin-top: 10px;
  border: none;
  padding: 5px 0px;
  background: white;
  color: black;
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;

  position: relative;
  bottom: 300px;
  animation: drop 1s linear forwards;
  animation-timing-function: ease;
}
.contact form input::-webkit-input-placeholder{
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  color: mediumaquamarine;
}
.contact form .feedback{
  color: white;
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  margin-top: 10px;
}

/* responsive design */
@media all and (max-width: 991px){
  .contact h1{
    font-size: 40px;
  }
}

@media all and (max-width: 768px){
  .contact h1{
    font-size: 40px;
  }
  .contact form button{
    width:50%;
  }
  .contact form {
    width: 100%;
  }
}

@media all and (max-width: 575px){
  .contact h1{
    font-size: 35px;
  }
}

/* animations */
@keyframes skew{
  from{
    transform: rotateY(90deg);
  }
  to{
    transform: rotateY(0deg);
  }
}

@keyframes drop{
  from{
    top: -300px;
  }
  to{
    top: 0px;
  }
}
</style>