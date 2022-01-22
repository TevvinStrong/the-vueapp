<template>
    <div class="text-input-container">
        <input
            class="text-input"
            type="text"
            :id="id"
            :placeholder="placeholder"
            :value="value"
            v-on:input="updateInputValue($event.target.value)"
        >
    </div>
</template>

<script>
export default {
    props: {
        id: {
            type: String
        },
        placeholder: {
            type: String
        },
        value: {
            type: String
        },
        height: {
            type: Number,
            default: 100
        }
    },
    methods: {
        updateInputValue: function (value) {
            this.$emit('input', value)
        }
    }
}
</script>

<style scoped>
    @import url('https://fonts.googleapis.com/css2?family=Raleway:wght@100&display=swap');
    .text-input-container {
        text-align: center;
        width: 100%;
        height: 100px;        
    }
    .text-input {
        font-size: 50px;
        font-family: 'Raleway', sans-serif;
        width: 500px;
        height: 100px;
    }
</style>