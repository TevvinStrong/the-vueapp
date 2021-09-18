<template>
  <div id="memeGenerator">
    <MemeGeneratorHeader />
    <MemeGeneratorImage />
  </div>
</template>

<script>
import MemeGeneratorHeader from './components/Header/Header.vue';
import MemeGeneratorImage from './components/MemeImage/MemeImage.vue';

export default {
  name: 'App',
  components: {
    MemeGeneratorHeader,
    MemeGeneratorImage
  }
}
</script>

<style>
  #memeGenerator {
    margin: auto;
    width: 800px;
    height: 963px;
    display: flex;
    justify-content: flex-start;
    flex-direction: column;
  }
</style>
