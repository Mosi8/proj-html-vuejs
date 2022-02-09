<template>
  <div class="header">
    <div class="container">
    <div class="row justify-content-center">
      <div class="col-3">
        <a href="#" class="textHeader me-2">Download App</a>
        <span class="bottios me-3">iOS</span>
        <a href="#" class="textHeader">Advertise with us</a>
      </div>
      <div class="col-6 text-center">
        <Logo :immagine="logoheader"/>
      </div>
      <div class="col-3">
        <a href="#" class="logoSocial ms-3 me-3">
          <i class="fa-brands fa-facebook-f"></i>
          <span class="nomiSocial">Facebook</span>
        </a>
        <a href="#" class="logoSocial ms-3 me-3">
          <i class="fa-brands fa-instagram"></i>
          <span class="nomiSocial">Instagram</span>
        </a>
        <a href="#" class="logoSocial ms-3 me-3">
          <i class="fa-brands fa-twitter"></i>
          <span class="nomiSocial">Twitter</span>
        </a>
        <a href="#" class="logoSocial ms-3 me-3">
          <i class="fa-brands fa-youtube"></i>
          <span class="nomiSocial">Youtube</span>
        </a> 
      </div>
      <div class="col-8 text-center">
        <ul>
          <li><a href="#" class="active">Home</a></li>
          <li v-for="(element, index) in menu" :key="index"><a href="#">{{element}}</a></li>
        </ul>
      </div>
    </div>
  </div>
  </div>
</template>

<script>
import Logo from '../commons/Logo.vue'
import vocimenu from '../../assets/data/vocimenu.js'

export default {
  name: 'Header',
  components: { 
    Logo 
  },
  data(){
        return {
            logoheader: require('../../assets/img/avada-food-logo-2x.png'),
            menu: vocimenu,
        }
  }
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/variables.scss';

.header {
  background-color: $secondColor;
  padding: 30px 0;

  .textHeader {
    color: #000;
    text-decoration: none;
    font-size: 13px;
  }
  .logoSocial {
    color: #000;
    text-decoration: none;
    font-size: 15px;
    position: relative;
    text-align: center;
  }

  .logoSocial:hover .nomiSocial {
    display: block;
  }
  .nomiSocial {
    position: absolute;
    top: 20px;
    left: 0px;
    transform: translateX(-30%);
    display: none;
    font-size: 12px;
  }
  .bottios {
    background-color: $mainColor;
    color: #fff;
    padding: 3px 5px;
    border-radius: 5px;
    font-size: 10px;
  }

  .col-6 {
    height: 130px;
    overflow: hidden;
  }

  .col-8 {
    ul {
      list-style-type: none;
      margin: 30px 0;
      li {
        display: inline;
        
        a {
          text-decoration: none;
          color: #000;
          transition: .4s;
          padding: 15px 10px;
          margin: 10px 30px;
        }
      }

      a:hover, .active {
        color: $mainColor;
        border-bottom: solid 2px $mainColor;
      }
    }
  }

}

</style>