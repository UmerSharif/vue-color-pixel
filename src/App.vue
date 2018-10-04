<template>
    <div id="app">
        <ColorPicker/>
        <Canvas />
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

        display: flex;
        justify-content: center;
        align-items: center;
    }

</style>
