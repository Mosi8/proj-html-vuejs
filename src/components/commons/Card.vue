<template>
    <div>
        <div class="interno">
            <div class="immagine">
                <img :src="require('../../assets/img/'+prova.img)">
            </div>
            <span>{{prova.name}}</span>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Card',
    props: {
        prova: Object
    },

}
</script>

<style lang="scss" scoped>
@import '../../assets/style/variables.scss';
.interno {
    background-color: #fff;
    padding: 7px;
    span {
        display: block;
        text-transform: uppercase;
        margin-top: 5px;
        padding: 10px 0;
        cursor: pointer;
    }
    span:hover{
        color: #fff;
        background-color: $mainColor;
    }
    .immagine {
        width: 100%;
        padding: 0px 60px;
        img {
        width: 80%;
        transition: 1s;
        cursor: pointer;
        }
        img:hover {
            transform: scale(1.2);
        }
    }
    
}
</style>