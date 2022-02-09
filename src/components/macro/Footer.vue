<template>
  <div>
      <div class="container">
          <div class="row">
              <div class="col-3 mborder">
                  <Logo :immagine="logoFooter" class="logofoot"/>
                  <div class="social">
                    <a href="#" class="logoSocial ms-2 me-2">
                        <i class="fa-brands fa-facebook-f"></i>
                        <span class="nomiSocial">Facebook</span>
                    </a>
                    <a href="#" class="logoSocial ms-2 me-2">
                        <i class="fa-brands fa-instagram"></i>
                        <span class="nomiSocial">Instagram</span>
                    </a>
                    <a href="#" class="logoSocial ms-2 me-2">
                        <i class="fa-brands fa-twitter"></i>
                        <span class="nomiSocial">Twitter</span>
                    </a>
                        <a href="#" class="logoSocial ms-2 me-2">
                        <i class="fa-brands fa-youtube"></i>
                    <span class="nomiSocial">Youtube</span>
                    </a> 
                  </div>
              </div>
              <div class="col-3 px-4 mborder">
                <ul class="menufoot">
                    <li v-for="(element, index) in menu" :key="index"><a href="#">{{element}}</a></li>
                </ul>
              </div>
              <div class="col-3 px-4 mborder">
                  <h6>CONTACT</h6>
                  
              </div>
              <div class="col-3 px-4">
                  <h6>GET OUR APP!</h6>
                  <div class="downfooter">
                        <img src="../../assets/img/download-app-store.png">
                        <img src="../../assets/img/download-android.png"> 
                  </div>
              </div>
          </div>
      </div>
      <div class="fondopagina text-center">
          <span>&copy; Copyright 2012 - 2022 | Avada Theme by ThemeFusion | All Rights Reserved | Powered by WordPress</span>
      </div>
  </div>
</template>

<script>
import Logo from '../commons/Logo.vue'
import vocimenu from '../../assets/data/vocimenu.js'

export default {
    name: 'Footer',
    components: {
        Logo,
    },
    data(){
        return {
            logoFooter: require('../../assets/img/avada-food-logo-mob-2x.png'),
            menu: vocimenu,
        }
    }

}
</script>

<style lang="scss" scoped>
@import '../../assets/style/variables.scss';

    .mborder {
        border-right: dashed 1px #afafaf;
    }
    .row {
        padding: 70px 0;
        height: 380px;
        color: $mainColor;

        .logofoot{
            height: 40%;
            padding: 5px 35px;
        }
        .social {
            margin: 30px 0;
            padding: 5px 35px; 
        }
        .logoSocial {
            color: #afafaf;
            text-decoration: none;
            font-size: 20px;
            position: relative;
            text-align: center;
        }

        .logoSocial:hover .nomiSocial {
            display: block;
        }
        .nomiSocial {
            position: absolute;
            top: 25px;
            left: 0px;
            transform: translateX(-30%);
            display: none;
            font-size: 12px;
        }

        .menufoot {
            margin: 0;
            list-style-type: none;
            li {
                padding: 10px 0;
                a {
                    text-decoration: none;
                    color: #000;
                    padding: 10px 0;
                }
            }
            li:hover a{
                color: $mainColor;
            }
        }

        h6 {
            letter-spacing: 2px;
        }
        .downfooter {
            height: 100%;
            img {
                margin: 5px 0;
                width: 100%;
            }
        }
    }
    .fondopagina {
        background-color: $secondColor;
        font-size: 12px;
        line-height: 12px;
        padding: 30px 0;
    }
</style>