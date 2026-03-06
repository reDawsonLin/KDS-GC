<script setup lang="ts">
definePageMeta({
  title: '食譜庫',
})
</script>

<template>
  <div>
    <div class="flex items-center justify-between mb-6">
      <h2 class="text-2xl font-bold">
        食譜庫
      </h2>
      <NuxtLink to="/recipes/new" class="btn-primary">
        新增食譜
      </NuxtLink>
    </div>

    <div class="card p-8 text-center">
      <div class="i-carbon-book text-4xl text-gray-300 mx-auto mb-3" />
      <p class="text-gray-400">
        串接 Supabase 後即可管理食譜
      </p>
    </div>
  </div>
</template>
