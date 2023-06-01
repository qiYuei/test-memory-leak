<template>
  <el-input-number
    v-model="num"
    :min="1"
    :max="10"
    @change="handleChange"
    custom
    v-for="(i, key) in 20"
    :key="key"
  />
</template>

<script lang="ts" setup>
import { onBeforeUnmount, ref } from 'vue'

const num = ref(1)
const handleChange = (value: number) => {
  console.log(value)
}

onBeforeUnmount(() => {
  console.log('unmounting.....')
})
</script>
