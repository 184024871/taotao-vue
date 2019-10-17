<!-- 首页轮播图组件 -->

<template>
    <div class="banner">
        <wv-swipe :height="130" :autoplay="4000">
            <wv-swipe-item style="background-color: #f44336">
                <img :src="bannerImg[0].src1" :alt="bannerImg[0].title1" width=100% height=100%>
            </wv-swipe-item>
            <wv-swipe-item style="background-color: #ffc107">
                <img :src="bannerImg[1].src2" :alt="bannerImg[1].title2" width=100% height=100%>
            </wv-swipe-item>
            <wv-swipe-item style="background-color: #03a9f4">
                <img :src="bannerImg[2].src3" :alt="bannerImg[2].title3" width=100% height=100%>
            </wv-swipe-item>
        </wv-swipe>
    </div>
</template>

<script>
    export default {
        name: 'Banner',
        data () {
            return {
                bannerImg: [
                    {src1: "./static/images/mm.jpg", title1: "美眉"},
                    {src2: "./static/images/xyj.jpg", title2: "洗衣机"},
                    {src3: "./static/images/yyy.jpg", title3: "营养液"}
                ]
            }
        }
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>

