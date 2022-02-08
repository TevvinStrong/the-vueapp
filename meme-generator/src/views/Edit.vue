<template>
  <div class="edit">
    <Header text="Edit Your Meme" id="main-header"/>
    <Editor :imageUrl="imageUrl"/>
  </div>
</template>

<script>
import Editor from '@/components/ui/editor/Editor.vue';
import Header from '@/components/layout/Header.vue';


export default {
  name: 'Edit',
  props: {
    imageUrl: String,
  },
  components: {
    Editor,
    Header
  },
}
</script>
