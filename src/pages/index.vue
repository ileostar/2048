<script setup lang="ts" generic="T extends any, O extends any">
defineOptions({
  name: 'IndexPage',
})

const gameScene = ref([
  [0, 0, 0, 2],
  [0, 0, 0, 2],
  [0, 0, 0, 2],
  [0, 0, 0, 2],
])
</script>

<template>
  <div flex="~ col" items-center justify-center>
    <h1 my5 text-4xl font-bold>
      2048
    </h1>
    <div border="2 solid gray-500/30" flex="~ col" gap-1 rd-1 p1>
      <div v-for="x, i in gameScene" :key="i" flex gap-1>
        <div v-for="y, k in x" :key="k" bg="gray-500/30" h-18 w-18 flex items-center justify-center rd-1 text-2xl>
          {{ y }}
        </div>
      </div>
    </div>
  </div>
</template>
