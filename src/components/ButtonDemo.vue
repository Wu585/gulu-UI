<template>
  <div>Button示例</div>
  <h1>示例1</h1>
  <div>
    <Button>你好</Button>
    <Button theme="button">你好</Button>
    <Button theme="link">你好</Button>
    <Button theme="text">你好</Button>
  </div>
  <h1>示例2</h1>
  <div>
    <Button>你好</Button>
    <Button size="big">大大大</Button>
    <Button size="normal">普通</Button>
    <Button size="small">小小小</Button>
  </div>
  <h1>示例3</h1>
  <div>
    <Button>你好</Button>
    <Button level="main">主要文字</Button>
    <Button level="normal">普通文字</Button>
    <Button level="danger">危险文字</Button>
  </div>
  <h1>示例4</h1>
  <Button disabled>禁用按钮</Button>
  <Button theme="link" :disabled="true">禁用链接按钮</Button>
  <Button theme="text" disabled>禁用按钮</Button>
  <h1>示例5</h1>
  <Button loading>加载中</Button>

</template>

<script lang="ts">
import Button from '../lib/Button.vue';

export default {
  components: {Button},
  setup() {
    const onClick = () => {
      console.log('hi');
    };
    return {onClick};
  }
};
</script>

<style lang="scss" scoped>

</style>