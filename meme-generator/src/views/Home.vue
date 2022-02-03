<template>
  <div class="home">
    <MemeGeneratorHeader text="Meme Machine" id="main-header"/>
    <Carousel />
    <TextInput v-model="inputText" placeholder="type input here!"></TextInput>
    <!-- purely for sake of testing input from child -->
    <p id="input-example"> i'm in the parent component!: {{ inputText }}</p>
  </div>
</template>


<script>
  import Carousel from '@/components/ui/carousel/Carousel.vue';
  import MemeGeneratorHeader from '@/components/layout/Header.vue';
  import TextInput from '@/components/ui/TextInput.vue';

  export default {
    name: 'Home',
    props: {
      inputText: {
        type: String
      }
    },
    components: {
      Carousel,
      MemeGeneratorHeader,
      TextInput
    }
  }
</script>

<style scoped>
  #meme-generator {
    display: flex;
    flex-direction: column;
    justify-content: center;
  }
  #text-input-container, #input-example {
    text-align: center;
  }
</style>
