<script setup lang="ts">
import { useTitle } from '@vueuse/core'

defineOptions({
  name: 'IndexPage',
})

const avaliable_works = [
  {
    no: '001',
    name: 'plum',
  },
  {
    no: '002',
    name: 'test',
  },
  {
    no: '003',
    name: 'test3',
  },
  {
    no: '004',
    name: 'test4',
  },

]

useTitle('100 days')
</script>

<template>
  <div>
    <h1 mb-2 mb-4 text-lg font-bold font-mono>
      100 days
    </h1>
    <pre class="grid grid-cols-1 gap-x-4 gap-y-1 lg:grid-cols-3 sm:grid-cols-2">
      <RouterLink v-for="work of avaliable_works" :key="work.no" :to="`/${work.no}`">
        <span> {{ work.no }}</span>
        <b>{{ work.name }}</b>
      </RouterLink>
    </pre>
  </div>
</template>

<route lang="yaml">
meta:
  layout: home
</route>

<style scoped>
pre {
    white-space-collapse: preserve;
    text-wrap: nowrap;
    font-size: 1em;
    font-family: Fira Code,Menlo,Monaco,Consolas,Liberation Mono,Courier New,monospace;
    justify-content: start; /* 左对齐 */
}
</style>
