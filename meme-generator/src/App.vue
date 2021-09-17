<template>
  <div id="memeGenerator">
    <MemeGeneratorHeader />
  </div>
</template>

<script>
import MemeGeneratorHeader from './components/Header/Header.vue';

export default {
  name: 'App',
  components: {
    MemeGeneratorHeader
  }
}
</script>

<style>
  #memeGenerator {
    height: 963px;
    display: flex;
    justify-content: center;
  }
</style>
