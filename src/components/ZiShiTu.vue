<template>
  <div>
    <h1>子视图</h1>
    <button @click="changeFather">子视图按钮点击穿值给父视图</button>
  </div>
</template>

<script>
import connect from '../js/eventBus'

export default {
    data() {
        return {
            dianying: '狂飙',
            dianshiju: '铁道有熊队',
            zongyi:'奔跑吧!code'
        }
    },
    created() {
    //    接收从父视图传过来的参数
        connect.$on('activeName', (item0, item1, item2, item3) => {
            console.log('从父视图传过来的值:', item0, item1, item2, item3);
        });
    },
    methods: {
        changeFather() {//触发按钮将值传给父视图
            this.$emit("changeEvent", this.dianying);
        }
    },
}
</script>

<style>

</style>