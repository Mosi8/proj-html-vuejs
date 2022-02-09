<template>
    <div class="main">
        <div class="jumbotron">
            <img src="../../assets/img/single-post-img3.jpg">
            <div class="corpojumbo">
                <div class="titolojumbo">
                    TODAY'S PICKS
                </div>
                <span>Food Corner: Top Japanese Restaurants for Sushi</span>
            </div>
        </div>
        <div class="container">
            <Popular />
        </div>
        
        <!-- cards  -->
        <div class="container">
            <div class="row justify-content-center">
                <div class="col-6 text-center">
                    <h5>culinary collection</h5>
                    <span>Aliquam erat volutpat. Ut quis ligula a magna blandit finibus. Suspendisse maximus lacus non nunc lacinia lobortis.</span>
                </div>
            </div>
            <div class="row mb-5">
                <Card class="col-3 text-center g-5" v-for="(element, index) in culinary" :key="index" :prova="element"/>
            </div>
        </div>
        <Subscribe />
    </div>
</template>

<script>
import Card from '../commons/Card.vue'
import Subscribe from '../sections/Subscribe.vue'
import culinarydata from '../../assets/data/culinarydata.js'
import Popular from '../sections/Popular.vue'

export default {
    name: 'Main',
    components: { 
        Subscribe,
        Card,
        Popular,
    },
    data(){
        return {
            culinary: culinarydata,
        }
    }

}
</script>

<style lang="scss" scoped>
@import '../../assets/style/variables.scss';

.main {
    background-color: $secondColor;

    .jumbotron {
        width: 100%;
        height: 600px;
        overflow: hidden;
        position: relative;
        margin-bottom: 50px;
        
        img {
            width: 100%;
            position: relative;
            top: -100px;
        }
        .corpojumbo {
            background-color: #fff;
            border-radius: 15px;
            min-width: 700px;
            min-height: 200px;
            position: absolute;
            top: 25%;
            left: 50%;
            transform: translateX(-50%);
            text-align: center;

            .titolojumbo {
                padding: 10px 30px;
                font-size: 15px;
                border-radius: 10px;
                color: #fff;
                background-color: $mainColor;
                position: absolute;
                top: 0;
                left: 50%;
                transform: translate(-50%,-50%);
            }   
            span {
                display: inline-block;
                width: 500px;
                font-size: 40px;
                margin-top: 40px;
            }
        }
    }

    h5 {
        text-transform: uppercase;
        font-size: 18px;
        margin-bottom: 30px;
    }
}
</style>