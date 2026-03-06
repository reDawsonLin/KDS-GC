<script setup lang="ts">
const nav_items = [
  { label: '今日總覽', icon: 'i-carbon-dashboard', to: '/' },
  { label: '食譜庫', icon: 'i-carbon-book', to: '/recipes' },
  { label: '今日菜單', icon: 'i-carbon-restaurant', to: '/menu' },
  { label: '備料看板', icon: 'i-carbon-task', to: '/prep' },
  { label: '備料總覽', icon: 'i-carbon-list-checked', to: '/prep/overview' },
]

const admin_items = [
  { label: '成員管理', icon: 'i-carbon-user-multiple', to: '/admin/members' },
  { label: '操作紀錄', icon: 'i-carbon-activity', to: '/admin/logs' },
]

const is_sidebar_open = ref(true)

function toggleSidebar() {
  is_sidebar_open.value = !is_sidebar_open.value
}
</script>

<template>
  <div class="min-h-screen bg-gray-50 dark:bg-gray-900 text-gray-900 dark:text-gray-100">
    <!-- Mobile header -->
    <header class="lg:hidden fixed top-0 left-0 right-0 z-50 bg-white dark:bg-gray-800 border-b border-gray-200 dark:border-gray-700 px-4 py-3 flex items-center gap-3">
      <button class="p-1" @click="toggleSidebar">
        <div class="i-carbon-menu text-xl" />
      </button>
      <h1 class="font-bold text-lg">
        KDS-GC
      </h1>
    </header>

    <!-- Sidebar overlay (mobile) -->
    <div
      v-if="is_sidebar_open"
      class="lg:hidden fixed inset-0 z-40 bg-black/50"
      @click="toggleSidebar"
    />

    <!-- Sidebar -->
    <aside
      class="fixed top-0 left-0 z-50 h-full w-64 bg-white dark:bg-gray-800 border-r border-gray-200 dark:border-gray-700 flex flex-col transition-transform duration-300"
      :class="is_sidebar_open ? 'translate-x-0' : '-translate-x-full lg:translate-x-0'"
    >
      <div class="px-5 py-6 border-b border-gray-200 dark:border-gray-700">
        <h1 class="text-xl font-bold text-primary-600">
          KDS-GC
        </h1>
        <p class="text-sm text-gray-500 mt-1">
          廚房備料管理系統
        </p>
      </div>

      <nav class="flex-1 px-3 py-4 overflow-y-auto">
        <ul class="space-y-1">
          <li v-for="item in nav_items" :key="item.to">
            <NuxtLink
              :to="item.to"
              class="flex items-center gap-3 px-3 py-2.5 rounded-lg text-sm font-medium transition-colors hover:bg-gray-100 dark:hover:bg-gray-700"
              active-class="bg-primary-50 dark:bg-primary-900/20 text-primary-600 dark:text-primary-400"
              @click="is_sidebar_open = false"
            >
              <div :class="item.icon" class="text-lg" />
              {{ item.label }}
            </NuxtLink>
          </li>
        </ul>

        <div class="mt-6 pt-4 border-t border-gray-200 dark:border-gray-700">
          <p class="px-3 mb-2 text-xs font-semibold text-gray-400 uppercase tracking-wider">
            管理
          </p>
          <ul class="space-y-1">
            <li v-for="item in admin_items" :key="item.to">
              <NuxtLink
                :to="item.to"
                class="flex items-center gap-3 px-3 py-2.5 rounded-lg text-sm font-medium transition-colors hover:bg-gray-100 dark:hover:bg-gray-700"
                active-class="bg-primary-50 dark:bg-primary-900/20 text-primary-600 dark:text-primary-400"
                @click="is_sidebar_open = false"
              >
                <div :class="item.icon" class="text-lg" />
                {{ item.label }}
              </NuxtLink>
            </li>
          </ul>
        </div>
      </nav>

      <div class="px-3 py-4 border-t border-gray-200 dark:border-gray-700">
        <NuxtLink
          to="/display"
          class="flex items-center gap-3 px-3 py-2.5 rounded-lg text-sm font-medium bg-gray-900 dark:bg-gray-100 text-white dark:text-gray-900 hover:opacity-90 transition-opacity"
        >
          <div class="i-carbon-screen text-lg" />
          廚房大螢幕模式
        </NuxtLink>
      </div>
    </aside>

    <!-- Main content -->
    <main class="lg:ml-64 pt-14 lg:pt-0 min-h-screen">
      <div class="p-4 lg:p-8">
        <slot />
      </div>
    </main>
  </div>
</template>
