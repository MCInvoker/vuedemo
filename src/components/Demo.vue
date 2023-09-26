<template>
    <div>
        <!-- 渲染 Button 类型的组件 -->
        <element-comp type="button" @click="handleButtonClick">Click Me</element-comp>

        <!-- 渲染 Input 类型的组件 -->
        <element-comp type="input" v-model="inputValue"></element-comp>

        <!-- 渲染 Tag 类型的组件 -->
        <element-comp type="tag">Tag content</element-comp>
    </div>
</template>
  
<script>
import ElementComp from './ElementComp.vue';

export default {
    components: {
        ElementComp,
    },
    data() {
        return {
        inputValue: '',
        };
    },
    methods: {
        handleButtonClick(e) {
            console.log(e)
        // 处理按钮点击事件的逻辑
        },
    },
};
</script>
  