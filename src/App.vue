<template>
    <div class="container">
        <app-task-grid :tasks="tasks"></app-task-grid>
    </div>
</template>

<script>
import TaskGrid from './components/TaskGrid.vue'

export default {
    data: function () {
        return {
            tasks: [
                'Just task to do!'
            ],
            maxTasks: 10
        }
    },
    components: {
        appTaskGrid: TaskGrid
    }
}
</script>

<style>

</style>
