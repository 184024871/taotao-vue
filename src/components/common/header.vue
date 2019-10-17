<!-- 公共头部组件 -->

<template>
    <div class="header">
        <mt-header fixed :title="title"></mt-header>
    </div>
</template>

<script>
    export default {
        name: 'Header',
        data () {
            return {
                title: "淘淘商城"
            }
        }
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>

