<template>
    <div class="popular">
        <div class="row justify-content-center">
            <div class="col-6 text-center my-5">
                <h5>POPULAR RECIPES</h5>
                <span>Aliquam erat volutpat. Ut quis ligula a magna blandit finibus. Suspendisse maximus lacus non nunc lacinia lobortis.</span>
            </div>
        </div>
        <div class="row">
            <div class="col-6 p-4 principale">
                <div class="immagine">
                    <img src="../../assets/img/Yogurt-Nan-600x395.jpg">
                    <div class="info text-center">
                        <a href="#">
                            <div class="link">
                                <i class="fas fa-link"></i>
                            </div>
                            <div class="textlink">
                                Lunch Favourite with Salad, Naan And Beans
                            </div>
                        </a>
                    </div>
                </div>
                <div class="textprincipale">
                    <div class="titolo">
                        <h5>Lunch Favourite with Salad, Naan And Beans</h5>
                        <span>Bakery, Featured, Healthy, Latest Recipes, Staff Picks</span>
                    </div>
                    <div class="text">
                        Suspendisse at semper odio. Nam fringilla scelerisque tincidunt. Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Donec tincidunt posuere ornare. Phasellus placerat odio non feugiat sollicitudin. Integer vitae elementum ex. Sed porttitor, diam eget convallis volutpat, arcu tellus facilisis nulla, id dignissim orci leo id
                    </div>
                    <button>learn more</button>
                </div>
            </div>
            <div class="col-6 p-3">
                <div class="row">
                    <div class="col-6 p-2" v-for="(element, index) in popular" :key="index">
                        <Popcard :piatto="element"/>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import Popcard from '../commons/Popcard.vue'
import popular from '../../assets/data/data.js'

export default {
  components: { Popcard },
    name: 'Popular',
    data(){
        return {
            popular: popular,
        }
    }

}
</script>

<style lang="scss" scoped>
@import '../../assets/style/variables.scss';
    .popular {
        margin-bottom: 100px;
    }
    .principale {
        .immagine {
            position: relative;
            a {
                text-decoration: none;
                color: #fff;
            }
        }
        img {
            width: 100%;
        }
        .info {
            position: absolute;
            top: 0;
            background: linear-gradient(rgba(255,255,255,.3) ,$mainColor 70%);
            width: 100%;
            height: 100%;
            font-size: 18px;
            color: #fff;
            padding: 80px;
            display: none;

            .link {
                padding: 10px 14px;
                color: $mainColor;
                background: #fff;
                display: inline-block;
                border-radius: 50%;
            }
        }
        .textprincipale {
            padding: 40px;
            font-size: 23px;
            background-color: #fff;

            .titolo {
                padding-bottom: 20px;
                border-bottom: dotted 2px #afafaf;
                span {
                    display: inline-block;
                    font-size: 15px;
                }
            }
            .text {
                margin: 20px 0;
                color: #6a6a6a;
                font-size: 18px;
                line-height: 30px;
            }

            button {
                text-transform: uppercase;
                font-size: 11px;
                color: #fff;
                background-color: $mainColor;
                border: none;
                border-radius: 2px;
                padding: 9px 20px;
                margin-bottom: 20px;
            }
        }
        .immagine:hover .info{
            display: block;
        }
    }

</style>