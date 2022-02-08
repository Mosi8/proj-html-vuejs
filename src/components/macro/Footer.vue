<template>
  <div>
      <div class="container">
          <div class="row">
              <div class="col-3 mborder">
                  <Logo :immagine="logoFooter" class="logofoot"/>
              </div>
              <div class="col-3 px-4 mborder">
                  
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

export default {
    name: 'Footer',
    components: {
        Logo,
    },
    data(){
        return {
            logoFooter: require('../../assets/img/avada-food-logo-mob-2x.png'),
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
            width: 100%;
            padding: 5px 35px;
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
        background-color: #f6f7f1;
        font-size: 12px;
        line-height: 12px;
        padding: 30px 0;
    }
</style>