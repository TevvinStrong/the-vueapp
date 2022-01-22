<template>
    <div class="carousel-container">
        <CarouselImage id="image-1"/>
        <CarouselImage id="image-2"/>
        <CarouselImage id="image-3"/>
        <CarouselImage id="image-4"/>
        <CarouselImage id="image-5"/>
    </div>
</template>

<script>
    import CarouselImage from '@/components/ui/carousel/CarouselImage.vue';
    export default {
        components: {
            CarouselImage,
        }
    }
</script>

<style scoped>
    .carousel-container {
        display: flex;
        flex-direction: row;
    }
    /* Need to do this dynamically, prob some v-bind magic */
    #image-4, #image-5 {
        display: none;
    }
</style>