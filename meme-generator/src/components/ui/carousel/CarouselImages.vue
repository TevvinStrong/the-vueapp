<template>
    <div class="carousel-images">
        <div v-for="meme in this.currMemes" :key="meme.name"> 
            <CarouselImage :meme="meme" />
        </div>
    </div>
</template>

<script>
import CarouselImage from '@/components/ui/carousel/CarouselImage.vue';
import axios from 'axios';

export default {
    name: 'CarouselImages',
    components: {
        CarouselImage,
    },
    props: {
        index: Number
    },
    data() {
        return {
            allMemesFromAPI: [Object],
            errors: [Object],
            currMemes: [Object],
            numOfCurrMemes: [Number]
        }
    },
    methods: {
        handleNegativeIndex(index) {
            return index >= 0 ? index : index + this.allMemesFromAPI.length
        },
        setCurrentMemes() {
            for (var i = 0; i < this.numOfCurrMemes; i++) {
                this.$set(
                    this.currMemes, 
                    i, 
                    this.allMemesFromAPI[this.handleNegativeIndex(this.index + i)]
                )
            }
        }
    },
    created () {
        axios.get('https://api.imgflip.com/get_memes')
        .then(response => {
            this.allMemesFromAPI = response.data.data.memes
            this.$emit('setNumOfImages', this.allMemesFromAPI.length)
            this.numOfCurrMemes = 3
            this.setCurrentMemes()
        })
        .catch(e => {
            this.errors.push(e)
        })
    },
    watch: {
        index: function() {
            this.setCurrentMemes()
        }
    }
}
</script>

<style scoped>
    .carousel-images {
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;
        height: 500px;
    }
</style>