<template>
    <ul>
        <li v-for="(todo, index) in todos" :key="index" @click="deleteTodo(index)">{{ index }}. {{ todo }}</li>
    </ul>
</template>

<script>
    export default {
        name: "TodoList",
        props: ['todos'],
        methods: {
            deleteTodo(index) {
                this.$emit('delete-todo', index);
            },
        },
    }
</script>

<style scoped>

</style>