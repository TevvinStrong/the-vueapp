<template>
  <div class="editor">
    <Canvas :imageUrl="imageUrl" />
    <EditorUserInput />
  </div>
</template>

<script>
import Canvas from '@/components/ui/editor/Canvas.vue';
import EditorUserInput from '@/components/ui/editor/EditorUserInput.vue';

export default {
  name: 'Editor',
  props: {
    imageUrl: String,
  },
  components: {
    Canvas,
    EditorUserInput,
  },
}
</script>

<style scoped>
.editor {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-evenly;
    width: 100%;
}
</style>