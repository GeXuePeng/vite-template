<template>
  about页面
  counter {{ counter }}
  <el-button @click="add">增加</el-button>
</template>
<script setup lang="ts">
import useDemoStore from '@/store/demo';
import { storeToRefs } from 'pinia';

const demoStore = useDemoStore()
const { counter } = storeToRefs(demoStore)

const add = ()=>{
  demoStore.increment()
}

</script>