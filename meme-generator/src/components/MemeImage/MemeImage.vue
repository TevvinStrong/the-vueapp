<template>
    <div class="meme-image">
        <!-- <img src="https://cdn.kqed.org/wp-content/uploads/sites/38/2019/03/tomemeornot3-768x384.jpg" alt="Funny Picture/Funny meme"> -->
        <!-- <img :v-bind="image" alt="Image retuned from meme api"> -->
        <!-- <img :v-for="Images" alt="Images from API"> -->
        <li v-for="image in images" :key="image.id">
            {{ image.url }}
        </li>
    </div>
</template>

<script>
    export default {
  name: "MemeImage",
  data() {
    return {
      images: {}
    }
  },
  beforeMount(){
    this.getImages();
  },
  methods: {
    async getImages(){
      const res = await fetch('https://api.imgflip.com/get_memes');
      const image = await res.json();
      this.image = image.data.memes;
      console.log('>>>>>>>>>>', this.image);
    }
  }
};
</script>

<style scoped>
    .meme-image {
        width: 700px;
        height: 362px;
        border: 1px solid black;
    }
</style>