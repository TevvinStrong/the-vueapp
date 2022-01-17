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
    font-size: 64px;
    text-align: center;
    width: 100%;
    height: 75px;
    font-weight: normal;
    padding-top: 3%;
  }
</style>
