<template>
    <div class="col-sm-6 col-md-4 col-lg-3">
        <div class="panel panel-default">
            <div class="panel-body task">
                <slot></slot>
            </div>
        </div>
    </div>
</template>

<script>
</script>

<style>
.panel-body {
    font-family: 'Arizonia', cursive;
    font-size: 24px;
    color: #6e6e6e;
}

.task {
    cursor: pointer;
    border: 1px solid black;
}

.task:hover {
    background-color: #ffe2e2;
}
</style>