<template>
  <component :is="componentType" v-bind="$attrs" v-on="$listeners">
    <slot></slot>
  </component>
</template>

<script>
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'ElementComp',
  props: {
    type: {
      type: String,
      required: true,
    },
  },
  computed: {
    componentType() {
      switch (this.type) {
        case 'button':
          return 'el-button';
        case 'input':
          return 'el-input';
        case 'tag':
          return 'el-tag';
        default:
          return null;
      }
    },
  },
});
</script>
