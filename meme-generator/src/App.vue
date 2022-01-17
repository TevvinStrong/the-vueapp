<template>
  <div id="memeGenerator">
    <MemeGeneratorHeader />
     <TextInput />
  </div>
</template>

<script>
    import MemeGeneratorHeader from './components/layout/Header.vue';
    import TextInput from './components/ui/TextInput.vue';

export default {
  name: 'App',
  components: {
      MemeGeneratorHeader,
      // new
      TextInput
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
