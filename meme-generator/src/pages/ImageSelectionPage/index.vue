<template>
  <div id="meme-generator">
    <MemeGeneratorHeader text="Meme Machine" id="main-header"/>
    <TextInput v-model="inputText" placeholder="type input here!" id="input-text-component"></TextInput>
    <!-- purely for sake of testing input from child -->
    <p> i'm in the parent component!: {{ inputText }}</p>
  </div>
</template>

<script>
    import MemeGeneratorHeader from '@/components/layout/Header.vue';
    import TextInput from '@/components/ui/TextInput.vue';

  export default {
    name: 'ImageSelectionPage',
    props: {
      inputText: {
        type: String
      }
    },
    components: {
      MemeGeneratorHeader,
      TextInput
    }
  }
</script>

<style>
  #meme-generator {
    display: flex;
    flex-direction: column;
    justify-content: center;
  }
</style>
