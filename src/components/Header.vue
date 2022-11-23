<template>
    <div class="row">
        <div class="col-sm-12">
            <h3>Tasks on board</h3>
            <div class="progress">
                <div class="progress-bar bg-info" role="progressbar"
                    :style="{ width: (taskCount / maxTasks) * 100 + '%' }" aria-valuenow="50" aria-valuemin="0"
                    aria-valuemax="100">
                    {{ taskCount }} / {{ maxTasks }}
                </div>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    props: ['taskCount', 'maxTasks']
}
</script>
<style>

</style>