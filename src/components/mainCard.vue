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
           <li><a href="https://forms.gle/kT7jcuW8KxJg4rgy6">Send a request</a></li>   <!--Google forms lang sa sir but will put a forms inside the portfolio jud-->
          </ul>
        </nav>
      </div>
      
      <div class="content">
      <h2>Services that I offer</h2>
      <div class="services">
     <div class = "service">
      <img src="../assets/computer.png" alt="Computer Service">
            <h3>Computer Desktop Services</h3>
         

        </div> 
          
        <div class="service">
            <img src="../assets/laptop.png" alt="Laptop Service">
            <h3>Laptop Services</h3>
          </div>
         
        </div>
      </div>
    </div>

           <div class="expertise">
        <h2>Expertise</h2>
        <button class="button" @click="toggleExpertise">{{ showExpertise ? 'Back' : 'Show details' }}</button>

          <div v-show="showExpertise" class="info-container">
          <div class = "info-card">
          <p>Basic computer and laptop troubleshooting not to mention upgrading it's hardware.</p>
          </div>
        </div> 
      
        </div>
        <div class="about-me">
        <h2>About Me</h2>
        <button class="button" @click="toggleAboutMe">{{ showAboutMe ? 'Back' : 'Show Details' }}</button>
       
          <div v-show="showAboutMe" class="info-container">
          <div class = "info-card">
          <p><strong>Name:</strong> Craig P. Cabugason</p>
          <p><strong>Skills:</strong> Gaming, Computer Technician</p>
          <p><strong>Experience:</strong> 8 years in computer troubleshooting and repair </p>
          <p><strong>Interests:</strong> Gaming, Technology, Problem-solving</p> 
          </div>
        </div>      
        </div>
       
        <br>
        <button class="button" @click="toggleImage">Service fees</button> 
        <br>
        <transition name="fade"> 
          <div class="container-two" v-if="showImage">
            <div class="services">
              <img src="../assets/service.jpg" alt="Service Image">
            </div>
          </div>
        </transition>
      
  </template>
  
  <script>
  export default {
    data() {
      return {
        showImage: false,
        showAboutMe: false , 
        showExpertise: false,
        showDesktopImage: false, 
        showLaptopImage: false
        
    
      };
    },

    methods: {
      toggleImage() {
        this.showImage = !this.showImage; 
      }, 

      toggleAboutMe(){
        this.showAboutMe = !this.showAboutMe;
      }, 

      toggleExpertise(){
        this.showExpertise = !this.showExpertise;
      }
    },  

    toggleSampleImage(service) {
 if(service === 'desktop'){
  this.showDesktopImage = !this.showDesktopImage;
 }
 else if(service ==='laptop'){
  this.showLaptopImage = !this.showLaptopImage;
 }
    }
  };

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
  
  .info-container {
    background-color: #D78928; 
    padding: 20px;
    border-radius: 10px;
    margin-top: 10px;
  } 

  .info-card{

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
  
