<template>
    <div class="container">
        <app-new-task @taskAdded="newTask"></app-new-task>
        <app-task-grid :tasks="tasks"></app-task-grid>
        <div class="row">
            <div class="col-sm-12 text-center">
                <div class="alert alert-info">
                    Info: Click on Task to complete ot!
                </div>
            </div>
        </div>
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
