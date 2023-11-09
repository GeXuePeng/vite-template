
<template>
  <div>
    <span @click="linkto('home')">home</span> | <span @click="linkto('about')">about</span>
  </div>
  <RouterView></RouterView>
</template>
<script lang="ts" setup>
import { RouterView, useRouter } from 'vue-router';

const router = useRouter()

const linkto = (type: string) => {
  router.push({ path: type })
}
</script>
<style lang="scss" scoped>
span{
  cursor: pointer;
}
</style>
