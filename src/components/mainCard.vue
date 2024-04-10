<template>
    <div class="main-container">
      <div class="header">
        <div class="profile">
          <img src="../components/profile.jpg" alt="Profile Picture">
          <div class="profile-details">
            <h1>Craig P. Cabugason</h1>
            <h3>Computer Technician & a Gamer</h3>
          </div>
        </div>
        <nav class="navigation">
          <ul>
          <!---  <router-link> to = "/documentation">Documentation</router-link> --> <!-- To be continued on the final version AKA on the finals-->
            <li><a href="https://www.facebook.com/GrimReaper44444444444444444444/">Contact me</a></li>
           <li><a href="https://forms.gle/kT7jcuW8KxJg4rgy6">Send a request</a></li>   
          </ul>
        </nav>
      </div>
      <div class="content">
        <h2>Services that I offer</h2>
        <div class="services">
          <div class="service">
            <img src="../assets/computer.png" alt="Computer Service">
            <h3>Computer Desktop Services</h3>
          </div>
          <div class="service">
            <img src="../assets/laptop.png" alt="Laptop Service">
            <h3>Laptop Services</h3>
          </div>
        </div>
        <div class="expertise">
          <h2>Expertise</h2>
          <p>I specialize in troubleshooting hardware and software issues, system optimization, data recovery, and providing comprehensive support for various computer and laptop models.</p>
        </div>
        <div class="about-me">
          <h2>About Me</h2>
          <p>I know about a thing or two about computers</p>
          <button class="button" @click="toggleImage">Service fees</button>
        </div>
        <transition name="fade">
          <div class="container-two" v-if="showImage">
            <div class="services">
              <img src="../assets/service.jpg" alt="Service Image">
            </div>
          </div>
        </transition>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        showImage: false
      };
    },
    methods: {
      toggleImage() {
        this.showImage = !this.showImage; 
      }
    }
  }
  </script>
  
  <style scoped>

  body {
    font-family: 'Segoe UI', sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f4f4f4;
  }
  
  a {
    text-decoration: none;
    color: inherit;
  }
  

  .main-container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 20px;
  }
  
  .header {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  
  .profile {
    display: flex;
    align-items: center;
  }
  
  .profile img {
    width: 100px;
    height: 100px;
    border-radius: 50%;
    margin-right: 20px;
  }
  
  .navigation ul {
    list-style: none;
    display: flex;
  }
  
  .navigation li {
    margin-right: 20px;
  }
  
  .content {
    margin-top: 50px;
  }
  
  .services {
    display: flex;
    justify-content: space-around;
    margin-bottom: 50px;
  }
  
  .service {
    text-align: center;
  }
  
  .service img {
    width: 100px;
    height: 100px;
  }
  
  .expertise {
    margin-bottom: 50px;
  }
  
  .about-me {
    text-align: center;
  }
  
  .button {
    display: inline-block;
    padding: 10px 20px;
    background-color: #007bff;
    color: #fff;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    transition: background-color 0.3s ease;
  }
  
  .button:hover {
    background-color: #0056b3;
  }
  

  .fade-enter-active,
  .fade-leave-active {
    transition: opacity 0.5s;
  }
  
  .fade-enter,
  .fade-leave-to {
    opacity: 0;
  }
  </style>
  
