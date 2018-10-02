<template>
    <div class="colorpicker">
        <Pixel isInColorPicker color="white" :current="color == 'white' ? true : false"/>
        <Pixel isInColorPicker color="lightblue" :current="color == 'lightblue' ? true : false"/>
        <Pixel isInColorPicker color="blue" :current="color == 'blue' ? true : false" />
        <Pixel isInColorPicker color="darkblue" :current="color == 'darkblue' ? true : false" />
    </div>

</template>

<script>

    import Pixel from './Pixel'

    export default {
        name: 'ColorPicker',
        components: {
            Pixel
        },

        props : {
            color : String
        }


    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
