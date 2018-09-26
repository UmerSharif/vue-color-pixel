<template>
    <div class="pixel">
      
    </div>
</template>

<script>

    import {mapGetters, mapState, mapMutations} from 'vuex'

    export default {
        name: 'Pixel'
        

    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    .pixel {
        border: 1px solid lightgray;
        width: 30px;
        height: 30px;
        box-sizing: border-box;
    }
</style>
