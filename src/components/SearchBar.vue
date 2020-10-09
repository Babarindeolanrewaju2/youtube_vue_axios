<template>
<div>
    <input @input="onInput" />
</div>
</template>

<script>
export default {
    name: 'SearchBar',
    methods: {
        onInput: function (event) {
            // eslint-disable-next-line vue/custom-event-name-casing
            this.$emit('termChange', event.target.value);
        }
    }
};
</script>

<style scoped>
input {
    width: 75%;
}

div {
    text-align: center;
    margin: 20px;
}
</style>
