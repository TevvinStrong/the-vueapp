<template>
    <div class="carousel-image">
        <img v-on:click="imageClicked()" :src="meme.url" :alt="meme.name">
    </div>
</template>

<script>
export default {
    name: 'CarouselImage',
    props: {
        meme: null
    },
    data() {
        return {
            apiImageUrl: []
        }
    },
    methods: {
        imageClicked() {
            this.$router.push({
                name: 'Edit',
                params: {
                    imageUrl: this.meme.url
                }
            })
        }
    }
}
</script>

<style scoped>
.carousel-image {
    width: 100%;
    text-align: center;
}
.carousel-image img {
    width: 300px;
    margin: 20px;
}
</style>