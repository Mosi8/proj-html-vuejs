<template>
    <div class="container-fluid">
        <div class="row">
            <div class="col-3 p-0" v-for="(element, index) in popular" :key="index">
                <Popcard v-if="index <4" :piatto="element"/>
            </div>
        </div>
    </div>
</template>

<script>
import popular from '../../assets/data/data.js'
import Popcard from '../commons/Popcard.vue'
export default {
    name:'FInemain',
    components: {
        Popcard,
    },
    data(){
        return {
            popular: popular,
            valoremassimo: 3,
        }
    }


}
</script>

<style>

</style>