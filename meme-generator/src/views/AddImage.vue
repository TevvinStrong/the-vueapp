<template>
  <div class="add-image">
      <div class="image-url">
        <input class="addimage-url" type="url" placeholder="url">
      </div>
      <div class="custom-meme">
        <input class="top-text" type="url" placeholder="Top-Text">
        <img src="https://www.getbgd.com/wp-content/uploads/2017/05/placeholder-image.png" alt="placeholder image template">
        <input class="bottom-text" type="url" placeholder="Bottom-Text">
      </div>
      <button class="submit">Generate</button>
  </div>
</template>

<script>

export default {
  name: 'AddImage',
  props: {
  },
  components: {

  },
}
</script>

<style scoped>

</style>