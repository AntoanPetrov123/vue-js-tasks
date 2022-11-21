<template>
    <div class="row">
        <app-task v-for="task in tasks"> {{ task }}</app-task>
    </div>
</template>

<script>
import Task from './Task.vue';

export default {
    props: ['tasks'],
    components: {
        appTask: Task
    }
}
</script>

<style>

</style>