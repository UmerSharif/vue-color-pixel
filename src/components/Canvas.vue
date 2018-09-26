<template>
    <div class="canvas">
    <Pixel/>
    </div>
</template>

<script>

    //import {mapGetters, mapState, mapMutations} from 'vuex'
        import Pixel from './Pixel'
    export default {
        name: 'Canvas',
        components : {
            Pixel
        }

    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
