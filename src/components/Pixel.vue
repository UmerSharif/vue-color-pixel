<template>
    <div class="pixel">
        <div @click="handleClick" :class="['pixel', color , current ? 'current' : '']"></div>
    </div>
</template>

<script>

    //import {mapGetters, mapState, mapMutations} from 'vuex'

    export default {
        name: 'Pixel',
        props: {
            color: String,
            current: Boolean,
            isInColorPicker: Boolean,
            isInCanvas: Boolean,
            index : Number
        },

        methods: {
            handleClick() {
                if(this.isInColorPicker) {
                    this.$root.$emit('updateColor', this.color)
                    console.log(this.color)
                }

                if(this.isInCanvas) {
                this.$root.$emit('clickedPixel' , this.index)
                }
            }

        }


    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    .pixel {
        border: 1px solid lightgray;
        width: 30px;
        height: 30px;
        box-sizing: border-box;

        .current {
            border: 4px solid yellow;
        }
    }

    .white {
        background-color: white;
    }

    .lightblue {
        background-color: rgb(0, 188, 212);
    }

    .blue {
        background-color: rgb(3, 169, 244);
    }

    .darkblue {
        background-color: rgb(33, 150, 243);
    }
</style>
