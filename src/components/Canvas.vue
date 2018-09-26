<template>
    <div class="canvas">
        <div class="pixel-class">
        <Pixel v-for="i in 30*30" :key = "i" color="lightblue"/>
        </div>
    </div>
</template>

<script>

    //import {mapGetters, mapState, mapMutations} from 'vuex'
    import Pixel from './Pixel'

    export default {
        name: 'Canvas',
        components: {
            Pixel
        }

    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.canvas {

    display: flex;
    justify-content: center;
    align-items: center;

    .pixel-class {
        display: flex;
        flex-wrap: wrap;
        width: 900px;
    }


}
</style>
