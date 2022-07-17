<template>
  <div id="app">
    
    <header>
      <button class="fixeds">icon</button>
      <img src="data:image/png;base64,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" alt="">
    </header>
    <nav>
     <router-link class="wieghter" to="/">Waiter</router-link> 
     
      
      <router-link class="Order" to="/about">Order</router-link>
    </nav>
    <router-view/>

    <div class="menu">
     <nav class="nav-menu-header">
      <div class="title-menu">
       <h2>Delicious <br>
         food for you</h2>
      </div>
      <input type="search" name="" class="Menu-input-search">
     </nav>
     <div class="options">
       <router-link  class="Menu-input" to="">Foods</router-link>  

        <router-link class="Menu-input" to="">Drinks</router-link> 
         <router-link class="Menu-input" to="">Snacks </router-link> 
          <router-link class="Menu-input" to="">Sauce</router-link> 
        
     </div>
     <router-view/>
    </div>
  </div>
</template>
<script>


export default {
        data() {
            return {
               
            };
        }
    };
    

    
</script>
<style>
body{
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
header{
  width: 100%;
  height: 300px;
  background-color: orangered;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 0 0 40px 40px;
  position: sticky;
}
header img{
  width: 150px;
  height: 150px;
  border-radius: 50%;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  width: 100%;
  min-height: 100vh;
  background: url(@/assets/background.jpg);
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  
  

}

nav {
  height: 50px;
 
  display: flex;
  justify-content: center;
  align-items: center;
  flex-basis: 50%;
  margin: 40px 20px 0 0;
  
}

nav a {
  font-weight: bold;
  color: #2c3e50;
  margin-left: 20px;
 text-align: center;
 width: 150px;
 height: 90%;
 justify-content: center;
 line-height : 45px;
 background-color: orangered;
 color: aliceblue;
 text-decoration: none;
 border-radius: 20px;
 
  
  
}

nav a.router-link-exact-active {
  color: #2c3e50;
}
.home{
  height: 300px;
   display: flex;
  flex-direction: column;
   backdrop-filter: blur(5px);
  border-radius: 50px;
  margin-top: 10px;
}
.about{
  height: 300px;
  display: flex;
  flex-direction: column;
  backdrop-filter: blur(5px);
  border-radius: 50px;
  margin-top: 10px;
}
.btn{
  height: 50px;
  margin:10px ;
}
.btn button{
   width: 180px;
    height: 40px;
    border-radius: 20px;
    border: none;
    color: aliceblue;
    background-color: orangered;
    
    }
    input{
      width: 350px;
      height: 35px;
      border-radius: 20px;
      border: 0.001em solid orangered;
      background-color: transparent;
      
    }
    h1{
      letter-spacing: 5px;
    }
    h3{
      margin-bottom: 3px;
    }
    input::placeholder{
      color: black;
      text-align: center;
      font-family: sans-serif;
      font-size: 10px;
    }
    .fixed{
      position: fixed;
      width: 50px;
      height: 50px;
      background-color: black;
      border: none;
      border-radius: 0 15px 15px 0;
      color: white;
    }
    .fixeds{
      position: fixed;
      top: 0;
      left: 0;
      width: 50px;
      height: 50px;
      background-color: black;
      border: none;
      border-radius: 0 15px 15px 0;
      color: white;
    }
    .menu{
      position: fixed;
      top: 0;
      bottom: 0;
      left: 0;
      right: 0;
      background-color: rgb(251, 251, 251);
      display: none;
    }
    .options{
        width: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 20px;
        
        border-radius: 20px;
        height: 100px;
      }
      .Menu-input{
       text-decoration: none;
       width: 6em;
       height: 2em;
       font-family: 'Century Gothic',sans-serif;
       font-style: normal;
       font-weight: 400;
       font-size: 17px;
       color: rgb(112, 112, 112);
       position: relative;
       margin-top: 0.8em;
       cursor: pointer;
      }
      .Menu-input:hover{
        color: #FA4A0C;
        border-bottom: 3px solid #FA4A0C;

      }
      .Menu-input-search{
        border-color: black;
      }
      .nav-menu-header{
        width: 100%;
        display: flex;
        flex-direction: column;
        height: 30%;
      }
      .title-menu{
        width: 100%;
        text-align: left;
        padding-left: 50px;
      }
      .title-menu h2{
      
       letter-spacing: 2px;
       
      color: rgb(112, 112, 112);
      Font-family: "Century" , "Gothic",sans-serif;
      Font-style: "Regular";
      Font-size: 34px;
      Line-height: 100%;

      }

</style>
