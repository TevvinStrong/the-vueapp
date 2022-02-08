<template>
    <div class="carousel-arrows">
        <img v-on:click="arrowClicked(-1)" id="left-arrow" src="@/assets/left-arrow.png">
        <img v-on:click="arrowClicked(1)" id="right-arrow" src="@/assets/right-arrow.png">
    </div>
</template>

<script>
export default {
    name: 'CarouselArrows',
    methods: {
        arrowClicked(value) {
            this.$emit('arrowClicked', value)
        }
    }
}
</script>

<style scoped>
#left-arrow, #right-arrow {
    padding-bottom: 25px;
}
#left-arrow {
    padding-right: 25px;
}
#right-arrow {
    padding-left: 25px;
}
</style>