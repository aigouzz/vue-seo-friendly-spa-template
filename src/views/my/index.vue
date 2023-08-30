<template>
    <div class="my_index">
        <div class="my_index_top">
            我的页面
        </div>
        <div @click="goto">跳转首页</div>
    </div>
</template>
<script setup lang="ts">
  import { useMetaRoute } from '@/composables';
  import router from '@/router'

  useMetaRoute();
  const goto = () => {
    router.push({
        path: '/',
    })
  };
</script>
<style lang="scss" scoped>
.my_index{
    width: 100%;
    text-align: center;
    padding-top: 66px;
}
</style>