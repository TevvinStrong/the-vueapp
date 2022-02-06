<template>
    <div class="carousel-image-container">
        <img :src="meme.url" :alt="meme.name">
    </div>
</template>

<script>
export default {
    name: 'CarouselImage',
    props: {
        meme: Object
    }
}
</script>

<style scoped>
    .carousel-image-container {
        width: 100%;
        text-align: center;
    }
    .carousel-image-container img {
        width: 300px;
        margin: 20px;
    }
</style>