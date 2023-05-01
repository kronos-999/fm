<template>
  <ul role="list" class="divide-y divide-gray-100">
    <h2 class="text-xl my-6">{{ header }}</h2>
    <li v-for="item in items" :key="item.title" class="flex w-full justify-between gap-x-6 py-5">
      <div class="flex w-1/5 gap-x-4">
        <div class="min-w-0 flex-auto">
          <p class="text-sm font-semibold leading-6 text-gray-900">{{ item.title }}</p>
        </div>
      </div>
      <div class="hidden sm:flex sm:flex-col sm:w-4/5">
        <p v-for="i in item.subitems" :key="i" class="mt-1 text-xs leading-5 text-gray-500">
          <h2 class="font-md font-bold">{{ i.title }}</h2>
          <h3 class="font-sm font-sm">{{ i.subtitle }}</h3>
        </p>
      </div>
    </li>
  </ul>
</template>

<script setup>
const props = defineProps({
  items: Array,
  header: String
})
</script>