<template>
  <div class="fuqin">
    <h1>父视图</h1>
    <button @click="fuclick">父视图按钮点击穿值给子视图</button>
    <ZiShiTu class="zishitu" @changeEvent="changeMyString"></ZiShiTu>
  </div>
</template>

<script>
import ZiShiTu from './ZiShiTu.vue'
import connect from '../js/eventBus'

export default {
    data() {
        return {
            zhuname: '高启强',
            usname: '高启盛',
            hhname: '唐小龙',
            kkkl: '唐小虎',
        }
    },
    components: {
        ZiShiTu
    },
    methods: {
        fuclick() {//触发
            // 点击按钮将参数传递给子视图
            connect.$emit("activeName", this.zhuname, this.usname, this.hhname, this.kkkl);
        },
        changeMyString(val) {//从子视图传递过来的值
            console.log('电影:', val);
        }
    },
}
</script>

<style>
.fuqin{
    background-color: blueviolet;
    height: 100vh;
    width: 100%;
}
.zishitu{
    background-color: bisque;
    margin-top: 10em;
    height: 50vh;
    width: 100%;
}
</style>