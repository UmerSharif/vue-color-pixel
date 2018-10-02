<template>
    <div class="canvas">
        <div class="pixel-class">
            <!--the color prop is from app-->
            <Pixel v-for="(color, index) in pixels" :key="index" :color="color" :index=index isInCanvas/>
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
        },
        props : {
            pixels: Array
        }

    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.canvas {

    .pixel-class {
        display: flex;
        flex-wrap: wrap;
        width: 900px;
    }


}
</style>
