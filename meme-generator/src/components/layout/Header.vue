<template>
  <h1>{{ text }}</h1>
</template>

<script>
export default {
    props: {
        id: {
            type: String
        },
        text: {
            type: String
        }
    }
}
</script>

<style scoped>
  @import url('https://fonts.googleapis.com/css2?family=Raleway:wght@100&display=swap');
  h1 {
    font-family: 'Raleway', sans-serif;
    font-size: 96px;
    text-align: center;
    width: 100%;
    font-weight: normal;
    padding: 50px 0 0 0;
    margin: 0;
  }
</style>
