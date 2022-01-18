<template>
  <div id="image-selection-page">
    <ImageSelectionPage />
  </div>
</template>

<script>
  import ImageSelectionPage from '@/pages/ImageSelectionPage';

  export default {
    name: 'App',
    components: {
      ImageSelectionPage
    }
  }
</script>

<style>
  #image-selection-page {
    height: 100%; 
  }
</style>
