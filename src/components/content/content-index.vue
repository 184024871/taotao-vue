<!-- 首页内容组件 -->

<template>
    <div class="content">
        <wv-grid>
            <wv-grid-item :to="{name:'TZ'}">
                <p class="weui-grid__label">
                    <span slot="label">电子产品</span>
                </p>
            </wv-grid-item>
            <wv-grid-item :to="{name: 'Teacher'}">
                <p class="weui-grid__label">
                    <span slot="label">男装服饰</span>
                </p>
            </wv-grid-item>
            <wv-grid-item to="/">
                <p class="weui-grid__label">
                    <span slot="label">女装服饰</span>
                </p>
            </wv-grid-item>
            <wv-grid-item to="/">
                <p class="weui-grid__label">
                    <span slot="label">时尚单品</span>
                </p>
            </wv-grid-item>
            <wv-grid-item to="/">
                <p class="weui-grid__label">
                    <span slot="label">家庭装饰</span>
                </p>
            </wv-grid-item>
            <wv-grid-item to="/">
                <p class="weui-grid__label">
                    <span slot="label">男士鞋袜</span>
                </p>
            </wv-grid-item>
            <wv-grid-item :to="{name: 'Shop'}">
                <p class="weui-grid__label">
                    <span slot="label">女士鞋袜</span>
                </p>
            </wv-grid-item>
            <wv-grid-item to="/">
                <p class="weui-grid__label">
                    <span slot="label">耳机耳麦</span>
                </p>
            </wv-grid-item>
            <wv-grid-item to="/">
                <p class="weui-grid__label">
                    <span slot="label">虚拟游戏</span>
                </p>
            </wv-grid-item>
        </wv-grid>
    </div>
</template>

<script>
    export default {
        name: 'Content',
        data () {
            return {
                thumbSmall: "123"
            }
        }
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    .icon {
        vertical-align: -0.15em;
        fill: currentColor;
        overflow: hidden;
    }
</style>

