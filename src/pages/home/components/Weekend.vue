<template>
    <div>
        <div class="title">周末去那儿</div>
        <ul>
            <li class="item border-bottom" v-for="(item, index) of list" :key="item.id">
                <div class="item-img-wrapper">
                    <img :src="item.imgUrl" class="item-img">
                </div>
                <div class="item-info">
                    <p class="item-title">{{item.title}}</p>
                    <p class="item-desc">{{item.desc}}</p>
                </div>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    name: 'HomeWeekend',
    props: {
        list: Array
    }
    // data() {
    //     return {
    //         recommendList: [{
    //             id: '0001',
    //             imgUrl: 'http://img1.qunarzz.com/sight/source/1811/f3/86173f863bef61.jpg_r_640x214_52b003ac.jpg',
    //             title: '故宫',
    //             desc: '故宫故宫故宫故宫故宫故宫故宫故宫'
    //         }, {
    //             id: '0002',
    //             imgUrl: 'http://img1.qunarzz.com/sight/source/1811/f3/86173f863bef61.jpg_r_640x214_52b003ac.jpg',
    //             title: '故宫',
    //             desc: '故宫故宫故宫故宫故宫故宫故宫故宫'
    //         }, {
    //             id: '0003',
    //             imgUrl: 'http://img1.qunarzz.com/sight/source/1811/f3/86173f863bef61.jpg_r_640x214_52b003ac.jpg',
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
    .item-img-wrapper
        overflow: hidden
        height: 0
        padding-bottom: 36.5%
        .item-img
            width: 100%
    .item-info
        padding: .1rem
        .item-title
            line-height: .54rem
            font-size: .32rem
            ellipsis()
        .item-desc
            line-height: .4rem
            color: #ccc
            ellipsis()
</style>