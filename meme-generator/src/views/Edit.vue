<template>
  <div class="edit">
    <h1>Meme editor page</h1>
    <Editor :imageUrl="imageUrl"/>
  </div>
</template>

<script>
import Editor from '@/components/ui/editor/Editor.vue';

export default {
  name: 'Edit',
  props: {
    imageUrl: String,
  },
  components: {
    Editor,
  },
}
</script>
