<template>
     <div class="col-sm-6 col-md-4 col-lg-3">
        <div class="panel panel-default">
            <div class="panel-body quote text-center">
                <slot></slot>
            </div>
        </div>
    </div>
</template>

<script>
export default {

}
</script>

<style lang="scss">
.panel {
    margin-top: 15px;
 .panel-body {
        font-family: 'Arizonia', cursive;
        font-size: 24px;
        color: #6e6e6e;
    }
    .quote {
        cursor: pointer;
        padding: 15px;
        border-radius: 10px;
        &:hover {
            background: #ffe2e2;
        }

    }
}
</style>
