<template>
    <div class="new">
        我是子组件
        <button @click="sendMsg">我是按钮</button>
        {{str}}
    </div>
</template>

<script>
export default {
    data() {
        return {
            count: 0,
            str: 10
        }
    },
    methods: {
       sendMsg() {
           this.str++
           this.$emit('zxcv', this.str)  
       }
    }
    // props: ['num', 'sfs']

    // props: {
    //     num: String
    // }

    // props: {
    //     num: {
    //         // 类型
    //         type: Number,
    //         // 是否必传
    //         required: false,
    //         // 默认值
    //         default: 1000000000000000
    //     }
    // }
}
</script>

<style scoped>
    .new{
        width: 100%;
        height: 200px;
        background: orange;
    }
</style>