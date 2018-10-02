<template>
    <div id="app">
        <ColorPicker/>
        <Canvas :pixels=pixels />
        <router-view/>
    </div>
</template>
<script>
    import Canvas from './components/Canvas'
    import ColorPicker from './components/ColorPicker'
    const defaultColor = 'white'
    export default {
        name: 'App',
        components: {
            Canvas,
            ColorPicker
        },
        data() {
            return {
                color: defaultColor,
                pixels: Array(30 * 30)
                    .fill()
                    .map(() => defaultColor)
            }
        },

        mounted() {
            this.$root.$on('updateColor', (color) => {
                this.color = color
            })

            this.$root.$on('clickedPixel', (index) => {
                this.pixels.splice(index, 1 , this.color)
            })

        }

    }
</script>
<style lang="scss">
    #app {
        font-family: 'Avenir', Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
        color: #2c3e50;
        margin-top: 60px;
    }

</style>
