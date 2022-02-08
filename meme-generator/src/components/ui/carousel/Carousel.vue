<template>
    <div class="carousel">
        <CarouselImages :index="index" />
        <CarouselArrows @arrowClicked="handleArrowClicked"/>
    </div>
</template>

<script>
import CarouselImages from '@/components/ui/carousel/CarouselImages.vue';
import CarouselArrows from '@/components/ui/carousel/CarouselArrows.vue';

export default {
    name: 'Carousel',
    components: {
        CarouselImages,
        CarouselArrows
    },
    methods: {
        handleArrowClicked (value) {
            this.index += value
        }
    },
    data() {
        return {
            index: [Number]
        }
    },
    created () {
        this.index = 0
    }
}
</script>