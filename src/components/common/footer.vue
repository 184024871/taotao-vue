<!-- 公共底部组件 -->

<template>
    <div class="footer">
        <wv-tabbar style="position:fixed; bottom:0;">
            <wv-tabbar-item :to="{name: 'Index'}" is-on>
                <span slot="icon" style="display: inline-block; position: relative;">
                    <svg class="icon weui-tabbar__icon" aria-hidden="true">
                        <use xlink:href="#icon-shouye"></use>
                    </svg>
                    <wv-badge is-dot style="position: absolute;top: 0;left: 24px;">8</wv-badge>
                </span>
                    首页
            </wv-tabbar-item>
            <wv-tabbar-item to="/">
                <span slot="icon" style="display: inline-block; position: relative;">
                    <svg class="icon weui-tabbar__icon" aria-hidden="true">
                            <use xlink:href="#icon-news_icon"></use>
                    </svg>
                    <wv-badge style="position: absolute;top: -2px;right: -13px;">8</wv-badge>
                </span>
                    新货上市
            </wv-tabbar-item>
            <wv-tabbar-item :to="{name: 'Shop.Shopcart'}">
                <span slot="icon" style="display: inline-block; position: relative;">
                    <svg class="icon weui-tabbar__icon" aria-hidden="true">
                        <use xlink:href="#icon-gouwuche"></use>
                    </svg>
                    <wv-badge v-if="shopNum" style="position: absolute;top: -2px;right: -13px;">{{ shopNum }}</wv-badge>
                </span>
                    购物车
            </wv-tabbar-item>
            <wv-tabbar-item to="/">
                <span slot="icon" style="display: inline-block; position: relative;">
                    <svg class="icon weui-tabbar__icon" aria-hidden="true">
                            <use xlink:href="#icon-tubiaozhizuomobanyihuifu-"></use>
                    </svg>
                    <wv-badge is-dot style="position: absolute;top: 0;right: -6px;">8</wv-badge>
                </span>
                    我的
            </wv-tabbar-item>
        </wv-tabbar>
    </div>
</template>

<script>
    // 导入购物监听
    import connect from '../../../static/js/connect.js'
    import shopTools from '../../../static/js/shopTools.js'

    export default {
        name: 'Footer',
        data () {
            return {
                shopNum: shopTools.getShopCount()
            }
        },
        computed: {
            num (){
                return this.$store.state.num
            }
        },
        created (){
            const that = this;
            connect.$on("addCart", function (num){
                that.shopNum += num;
            })
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
    .footposition{
        position: fixed;
        bottom:0;
    }
</style>

