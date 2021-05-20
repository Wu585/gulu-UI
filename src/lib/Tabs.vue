<template>
  <div>
    Tabs组件
    <component v-for="c in defaults" :is="c"/>
  </div>
</template>

<script lang="ts">
import Tab from './Tab.vue';

export default {
  setup(props, context) {
    let defaults = context['slots'].default();
    defaults.forEach((tag) => {
      if (tag.type !== Tab) {
        throw new Error('Tabs 子标签必须是 Tab');
      }
    });
    return {defaults};
  }
};
</script>