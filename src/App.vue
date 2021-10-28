<template>
  <router-view #="{ Component }">
    <component :is="Component" />
  </router-view>
</template>

<script setup lang="ts">
import { useStore } from 'vuex'

const store = useStore()
const getLabelList = () => store.dispatch('label/getLabelList')
getLabelList()

console.log('app')
</script>
