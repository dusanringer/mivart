<template>
   
    <div class="menu">
      <p>MENU</p>
      <a @click.prevent="sendEvent" class="menu-icon" href="#">
        <img src="../assets/menu-rot.svg" alt="menu">
      </a>
      <img class="head" src="../assets/head.svg" alt="head">
      <div class="menu-first">
        <a href="">
        <img src="../assets/menu-01.jpg" alt="menu">
        </a>
        <a href="">
        <img src="../assets/menu-02.jpg" alt="menu">
        </a>
        <a href="">
        <img src="../assets/menu-03.jpg" alt="menu">
        </a>
      </div>
      <div class="menu-second">
        <a href="">
        <img src="../assets/menu-04.jpg" alt="menu">
        </a>
        <a href="">
        <img src="../assets/menu-05.jpg" alt="menu">
        </a>
        <a href="">
        <img src="../assets/menu-06.jpg" alt="menu">
        </a>
      </div>
    </div>
</template>

<script>
    export default {
          

        methods: {
         sendEvent(e) {
           this.$emit('click-button')
           
         }
       },

    }
</script>

<style lang="scss" scoped>

  $mainColor: #a39475;
  $borderColor: #d59aa4;


     .menu {
    background: #fff;
    width: 50vw;
    height: 100vh;
    position: fixed;
    top: 0;
    z-index: 150;
    box-shadow: rgba(0, 0, 0, 0.10) -60px 0 35px -15px inset; 
    
  }
  
  .head {
    max-width: 400px;
    display: block;
    position: relative;
    top: 100px;
    left: 0;
    z-index: 110;
  }

  .menu-icon {
    position: relative;
    display: inline-block;
    top: 0;
    left: 47%;
  }

  p {
    display: inline-block;
    position: absolute;
    left: 0;
    margin: 10px 0 0 10px;
  }

  .menu-first {
    position: absolute;
    display: flex;
    flex-direction: row;
    top: 200px;
    left: 100px;
    z-index: 115;
  }

  .menu-first img {
    width: 110px;
    height: auto;
    margin-right: 100px;
    border-radius: 50%;
    border: 3px solid $mainColor;
    opacity: .6;

    &:hover {
      border: 3px solid $borderColor;
      opacity: 1;
      transition: opacity .6s;
    }
  }

  .menu-second {
    position: absolute;
    display: flex;
    flex-direction: row;
    top: 450px;
    left: 100px;
    z-index: 114;
    
  }

  .menu-second img {
    width: 110px;
    height: auto;
    margin-right: 100px;
    border-radius: 50%;
    border: 3px solid $mainColor;
    opacity: .6;

    &:hover {
      border: 3px solid $borderColor;
      opacity: 1;
      transition: opacity .6s;
    }
  }
</style>