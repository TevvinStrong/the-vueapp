<template>
    <div id="text-input-container">
        <input
            class="input"
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
    #text-input-container {
        height: 30px;
    }
    #input {
        width: 500px;
    }
</style>