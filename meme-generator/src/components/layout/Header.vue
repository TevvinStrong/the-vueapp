<template>
  <h1>{{ text }}</h1>
</template>

<script>
export default {
    name: 'Header',
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
  font-weight: bold;
  padding: 25px 0;
  margin: 0;
}
</style>
