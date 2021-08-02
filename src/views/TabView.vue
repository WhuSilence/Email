<template>
    <div>
        <TabBar>
            <TabBarItem path="/home">
                <img slot="item-icon" src="@/assets/img/tabbar/Home.svg"/>
                <img slot="item-icon-activate" src="@/assets/img/tabbar/Home-activate.svg"/>
                <div slot="item-text">首页</div>
            </TabBarItem>
            <TabBarItem path="/category">
                <img slot="item-icon" src="@/assets/img/tabbar/class.svg"/>
                <img slot="item-icon-activate" src="@/assets/img/tabbar/class-activate.svg"/>
                <div slot="item-text">分类</div>
            </TabBarItem>
            <TabBarItem path="/car">
                <img slot="item-icon" src="@/assets/img/tabbar/car.svg"/>
                <img slot="item-icon-activate" src="@/assets/img/tabbar/car-activate.svg"/>
                <div slot="item-text">购物车</div>
            </TabBarItem>
            <TabBarItem path="/profile">
                <img slot="item-icon" src="@/assets/img/tabbar/mine.svg"/>
                <img slot="item-icon-activate" src="@/assets/img/tabbar/mine-activate.svg"/>
                <div slot="item-text">我的</div>
            </TabBarItem>
        </TabBar>
    </div>
</template>

<script>
    import TabBar from '@/components/common/TabBar/Tab-Bar'
    import TabBarItem from '@/components/common/TabBar/TabBarItem'
    export default {
        name: "TabView",
        components:{
            TabBar,
            TabBarItem
        }
    }
</script>

<style scoped>

</style>