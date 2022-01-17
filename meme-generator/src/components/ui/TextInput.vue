<template>
    <div id="TextInputContainer">
        <input v-model="message" placeholder="type here!">
        <p>hello {{ message }}</p>
    </div>
</template>

<script>
    export default {  
        data(){
            return { message: '' }
        }
    };
</script>

<style scoped>
    #TextInputContainer {
        height: 100px;
    }
</style>