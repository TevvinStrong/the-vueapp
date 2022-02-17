<template>
  <div class="marketing">
    <div class="nav-bar">
      <router-link class="link" to="/about">About</router-link>
      <router-link class="link" to="/generate">Generate Memes</router-link>
    </div>
  </div>
</template>


<script>
//Imports

export default {
  name: 'Marketing',
  props: {
  },
  components: {
  }
}
</script>

<style scoped>
.nav-bar {
    display: flex;
    flex-direction: row;
    justify-content: flex-end;
    margin-right: 3%;
    margin-top: 48px;
}

.link {
    color: #ffff;
    text-decoration: none;
    padding-right: 4%;
}
</style>
