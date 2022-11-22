<template>
    <div class="row">
        <!-- click.native allows us to click on component -->
        <app-task v-for="(task, index) in tasks" @click.native="completeTask(index)"> {{ task }}</app-task>
    </div>
</template>

<script>
import Task from './Task.vue';

export default {
    props: ['tasks'],
    components: {
        appTask: Task
    },
    methods: {
        completeTask(index) {
            this.$emit('taskCompleted', index);
        }
    }
}
</script>

<style>

</style>