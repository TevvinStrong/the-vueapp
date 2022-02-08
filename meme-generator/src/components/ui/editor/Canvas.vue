<template>
  <div class="canvas">
    <canvas id="memeCanvas" ref="memeCanvas"></canvas>
  </div>
</template>

<script>
export default {
  name: 'Canvas',
  props: {
    imageUrl: String
  },
  data() { 
    return {
      canvas: null,
      context: null,
      image: null,
    }
  },
  methods: {
    setupCanvasAndContext() {
      this.canvas = this.$refs.memeCanvas;
      this.canvas.width = 500;
      this.canvas.height = 500;
      this.context = this.canvas.getContext('2d');
    },
    drawImageToCanvas() {
      const scale = Math.min(this.canvas.width / this.image.width, this.canvas.height / this.image.height)
      const dWidth = this.image.width * scale;
      const dHeight = this.image.height * scale;
      const dx = this.image.width >= this.image.height ? 0 : (this.canvas.width / 2) -  (dWidth / 2);
      const dy = this.image.width >= this.image.height ? (this.canvas.height / 2) - (dHeight / 2) : 0;
      this.context.drawImage(this.image, dx, dy, dWidth, dHeight);
    },
    loadImage() {
      this.image = new Image();
      this.image.onload = () => {
        this.drawImageToCanvas();
      };
      this.image.src = this.imageUrl;
    },
  },
  mounted() {
    this.setupCanvasAndContext();
    this.loadImage();
  },
}
</script>