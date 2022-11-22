<template>
    <div class="container">
        <app-new-task @taskAdded="newTask"></app-new-task>
        <app-task-grid :tasks="tasks"></app-task-grid>
    </div>
</template>

<script>
import TaskGrid from './components/TaskGrid.vue';
import NewTask from './components/NewTask.vue';

export default {
    data: function () {
        return {
            tasks: [
                'Just task to do!'
            ],
            maxTasks: 10
        }
    },
    methods: {
        newTask(task) {
            this.tasks.push(task);
        }
    },
    components: {
        appTaskGrid: TaskGrid,
        appNewTask: NewTask
    }
}
</script>

<style>

</style>
