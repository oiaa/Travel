<template>
    <div>
        <div class="title">热销推荐</div>
        <ul>
            <router-link
                tag="li" 
                class="item border-bottom" 
                v-for="(item, index) of list" 
                :key="item.id"
                :to=" '/detail/' + item.id "
            >
                <img :src="item.imgUrl" class="item-img">
                <div class="item-info">
                    <p class="item-title">{{item.title}}</p>
                    <p class="item-desc">{{item.desc}}</p>
                    <button class="item-button">查看详情</button>
                </div>
            </router-link>
        </ul>
    </div>
</template>

<script>
export default {
    name: 'HomeRecommend',
    props: {
        list: Array
    },
    // data() {
    //     return {
    //         recommendList: [{
    //             id: '0001',
    //             imgUrl: 'http://img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_200x200_1bc99086.jpg',
    //             title: '故宫',
    //             desc: '故宫故宫故宫故宫故宫故宫故宫故宫'
    //         }, {
    //             id: '0002',
    //             imgUrl: 'http://img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_200x200_1bc99086.jpg',
    //             title: '故宫',
    //             desc: '故宫故宫故宫故宫故宫故宫故宫故宫'
    //         }, {
    //             id: '0003',
    //             imgUrl: 'http://img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_200x200_1bc99086.jpg',
    //             title: '故宫',
    //             desc: '故宫故宫故宫故宫故宫故宫故宫故宫'
    //         },]
    //     }
    // },
}
</script>

<style lang="stylus" scoped>
    @import '~styles/mixins.styl'
    .title
        line-height: .8rem
        background: #eee
        text-indent: .2rem
        margin-top: .2rem
    .item
        overflow: hidden
        display: flex
        height: 1.9rem
        .item-img
            width: 1.7rem
            height: 1.7rem
            padding: .1rem
        .item-info
            flex: 1
            padding: .1rem
            min-width: 0
            .item-title
                line-height: .54rem
                font-size: .32rem
                ellipsis()
            .item-desc
                line-height: .4rem
                color: #ccc
                ellipsis()
            .item-button
                background: #ff9300
                padding: 0 .2rem
                border-radius: .06rem
                margin-top: .16rem
                line-height: .44rem
                color: #fff
</style>