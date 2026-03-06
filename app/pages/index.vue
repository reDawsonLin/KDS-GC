<script setup lang="ts">
definePageMeta({
  title: '今日總覽',
})
</script>

<template>
  <div>
    <h2 class="text-2xl font-bold mb-6">
      今日總覽
    </h2>

    <div class="grid grid-cols-1 md:grid-cols-2 xl:grid-cols-4 gap-4 mb-8">
      <div class="card p-5">
        <div class="flex items-center gap-3 mb-2">
          <div class="w-10 h-10 rounded-lg bg-primary-100 dark:bg-primary-900/30 flex items-center justify-center">
            <div class="i-carbon-restaurant text-primary-600 text-xl" />
          </div>
          <p class="text-sm text-gray-500">
            今日菜單
          </p>
        </div>
        <p class="text-3xl font-bold">
          —
        </p>
      </div>

      <div class="card p-5">
        <div class="flex items-center gap-3 mb-2">
          <div class="w-10 h-10 rounded-lg bg-warning-400/20 flex items-center justify-center">
            <div class="i-carbon-task text-warning-600 text-xl" />
          </div>
          <p class="text-sm text-gray-500">
            備料進度
          </p>
        </div>
        <p class="text-3xl font-bold">
          —
        </p>
      </div>

      <div class="card p-5">
        <div class="flex items-center gap-3 mb-2">
          <div class="w-10 h-10 rounded-lg bg-blue-100 dark:bg-blue-900/30 flex items-center justify-center">
            <div class="i-carbon-user-multiple text-blue-600 text-xl" />
          </div>
          <p class="text-sm text-gray-500">
            上線人數
          </p>
        </div>
        <p class="text-3xl font-bold">
          —
        </p>
      </div>

      <div class="card p-5">
        <div class="flex items-center gap-3 mb-2">
          <div class="w-10 h-10 rounded-lg bg-green-100 dark:bg-green-900/30 flex items-center justify-center">
            <div class="i-carbon-book text-green-600 text-xl" />
          </div>
          <p class="text-sm text-gray-500">
            食譜總數
          </p>
        </div>
        <p class="text-3xl font-bold">
          —
        </p>
      </div>
    </div>

    <div class="grid grid-cols-1 lg:grid-cols-2 gap-6">
      <div class="card p-6">
        <h3 class="text-lg font-semibold mb-4">
          午餐菜單
        </h3>
        <p class="text-gray-400 text-sm">
          尚未設定今日菜單，串接 Supabase 後即可使用
        </p>
      </div>

      <div class="card p-6">
        <h3 class="text-lg font-semibold mb-4">
          晚餐菜單
        </h3>
        <p class="text-gray-400 text-sm">
          尚未設定今日菜單，串接 Supabase 後即可使用
        </p>
      </div>
    </div>
  </div>
</template>
