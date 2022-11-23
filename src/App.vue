<template>
    <div class="container">
        <app-new-task @taskAdded="newTask"></app-new-task>
        <app-task-grid :tasks="tasks" @taskCompleted="completeTask"></app-task-grid>
        <app-header :taskCount="tasks.length" :maxTasks="maxTasks"></app-header>
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
import Header from './components/Header.vue';

export default {
    data: function () {
        return {
            tasks: [
                'Just task to do!'
            ],
            maxTasks: 12
        }
    },
    methods: {
        newTask(task) {
            if (this.tasks.length >= this.maxTasks) {
                return alert('Please complete or delete task first!')
            }
            this.tasks.push(task);
        },
        completeTask(index) {
            this.tasks.splice(index, 1);
        }
    },
    components: {
        appTaskGrid: TaskGrid,
        appNewTask: NewTask,
        appHeader: Header
    }
}
</script>

<style>

</style>
