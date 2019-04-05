<template>
    <div>
        <div v-bind:key="todo.id" v-for="todo in todos">
            <ToDoItem v-bind:todo="todo"/>
        </div>
    </div>
</template>

<script>
import ToDoItem from './ToDoItem.vue';

export default { 
    name: "ToDos",
    components: {
        ToDoItem
    },
    props: ["todos"]
}
</script>

<style <style scoped>

</style>
