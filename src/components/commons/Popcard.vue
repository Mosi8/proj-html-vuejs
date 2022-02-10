<template>
    <div>
        <div class="interno">
            <div class="immagine">
                <img :src="require('../../assets/img/'+piatto.img)">
                <div class="info text-center">
                    <a href="#">
                        <div class="link">
                            <i class="fas fa-link"></i>
                        </div>
                        <div class="textlink">
                            {{piatto.title}}
                        </div>
                    </a>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Popcard',
    props: {
        piatto: Object
    },

}
</script>

<style lang="scss" scoped>
@import '../../assets/style/variables.scss';
.interno {
    width: 100%;
    height: 100%;
    
    .immagine {
        width: 100%;
        height: 100%;
        position: relative;
        
        img {
            width: 100%;
            height: 100%;
        }
        a{
            text-decoration: none;
            color: #fff;
        }
        .info {
            position: absolute;
            top: 0;
            background: linear-gradient(rgba(255,255,255,.3) ,$mainColor 70%);
            height: 100%;
            width: 100%;
            font-size: 18px;
            color: #fff;
            padding: 40px;
            display: none;

            .link {
                padding: 10px 14px;
                color: $mainColor;
                background: #fff;
                display: inline-block;
                border-radius: 50%;
            }
        }
    }

    .immagine:hover .info{
        display: block;
    }
    
    
}
</style>