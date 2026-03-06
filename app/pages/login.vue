<script setup lang="ts">
definePageMeta({
  title: '登入',
  layout: false,
})
</script>

<template>
  <div class="min-h-screen flex items-center justify-center bg-gray-50 dark:bg-gray-900">
    <div class="card p-8 w-full max-w-sm text-center">
      <h1 class="text-2xl font-bold text-primary-600 mb-2">
        KDS-GC
      </h1>
      <p class="text-gray-500 mb-8">
        廚房備料管理系統
      </p>

      <button class="btn w-full flex items-center justify-center gap-3 bg-white dark:bg-gray-700 border border-gray-300 dark:border-gray-600 hover:bg-gray-50 dark:hover:bg-gray-600">
        <div class="i-carbon-logo-google text-lg" />
        使用 Google 帳號登入
      </button>

      <p class="mt-6 text-xs text-gray-400">
        需經管理者授權才可使用
      </p>
    </div>
  </div>
</template>
