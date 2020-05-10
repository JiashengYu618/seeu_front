<template>
    <div class="header-bar">
        <span>Following</span>
        <span style="font-size:12px;padding-left:10px;padding-right:10px;padding-top:2px;display:block;line-height:18px;">|</span>
        <router-link tag="span" to="/videos-list">For U</router-link>
    </div>
</template>

<script>
export default {
    name:'HeaderBar',
    data(){
        return{

        };
    },
}
</script>

<style lang='stylus' scoped>
    .header-bar{
        z-index: 100;
      //  background-color:#000000;
        //border: 1px solid #FF2D2D;
        width:100%;
        height:50px; 
        position: absolute;
        top:35px;
        font-size:18px;
        left:0;
        text-align: center;
        display: flex;
        justify-content: center;//让中间的竖线seperator居中(middle)
        color:#ffffff;//text color
        opacity: 0.75;
    }
</style>