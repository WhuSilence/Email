<template>
    <div class="tab-bar-item" @click="itemClick">
        <slot v-if="!isActive" name="item-icon" ></slot>
        <slot v-else name="item-icon-activate"></slot>
        <div :class="{active:isActive}" :style=isActiveStyle>
            <slot name="item-text"></slot>
        </div>
    </div>

</template>

<script>
    export default {
        name: "TabBarItem",
        props:{
            path: String,
            activeColor:{
                type:String,
                default:'red'
            }
        },
        data(){
            return{

            }
        },
        computed:{
          isActive(){
              return this.$route.path.indexOf(this.path)!==-1
          },
          isActiveStyle(){
              return this.isActive?{color:this.activeColor}:{}
          }
        },
        methods:{
            itemClick(){
                console.log("itemClick");
                this.$router.replace(this.path)
            }
        }
    }
</script>

<style scoped>
    .tab-bar-item{
        flex: 1;
        text-align: center;
        height: 49px;
        font-size: 14px;
    }
    .active{
        color: red;
    }
    .tab-bar-item img{
        height: 24px;
        weight:24px;
        vertical-align: center;
        margin-top: 3px;

    }

</style>