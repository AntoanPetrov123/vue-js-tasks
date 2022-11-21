<template>
    <div class="row">
        <form action="">
            <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3 form-group">
                <label for="">Task</label>
                <textarea name="" id="" class="form-control" cols="30" rows="3" v-model="task"></textarea>
            </div>
            <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3 form-group">
                <!-- click.prevent = don't send request to a server -->
                <button class="btn btn-primary" @click.prevent="createNew">Add Task</button>
            </div>
        </form>
    </div>
</template>

<script>
export default {
    data: function () {
        return {
            task: ''
        };
    }
}
</script>

<style>

</style>