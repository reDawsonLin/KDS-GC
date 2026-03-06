<script setup lang="ts">
definePageMeta({
  title: '廚房大螢幕',
  layout: false,
})
</script>

<template>
  <div class="min-h-screen bg-gray-900 text-white p-8 font-sans">
    <header class="flex items-center justify-between mb-8">
      <h1 class="text-3xl font-bold">
        KDS-GC 廚房看板
      </h1>
      <div class="text-xl text-gray-400">
        {{ new Date().toLocaleDateString('zh-TW', { weekday: 'long', year: 'numeric', month: 'long', day: 'numeric' }) }}
      </div>
    </header>

    <div class="grid grid-cols-1 lg:grid-cols-2 gap-8">
      <div class="bg-gray-800 rounded-2xl p-6">
        <h2 class="text-2xl font-bold mb-4 text-green-400">
          午餐
        </h2>
        <p class="text-gray-500 text-lg">
          尚未設定菜單
        </p>
      </div>

      <div class="bg-gray-800 rounded-2xl p-6">
        <h2 class="text-2xl font-bold mb-4 text-blue-400">
          晚餐
        </h2>
        <p class="text-gray-500 text-lg">
          尚未設定菜單
        </p>
      </div>
    </div>

    <div class="mt-8 text-center">
      <NuxtLink to="/" class="text-gray-500 hover:text-gray-300 transition-colors">
        返回管理介面
      </NuxtLink>
    </div>
  </div>
</template>
