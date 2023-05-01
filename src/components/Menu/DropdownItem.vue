<template>
  <div class="contents">
    <Menu as="div" class="relative ml-3 flex">
      <div class="flex items-center">
        <a v-if="href" :href="href" class="text-gray-300 text-sm font-medium self-center">{{ title }}</a>
        <MenuButton v-if="!href" class="flex focus:outline-none">
          <span class="sr-only">Open user menu</span>
          <p class="text-gray-300 text-sm font-medium self-center">{{ title }}</p>
        </MenuButton>
      </div>
      <transition v-if="items.length" enter-active-class="transition ease-out duration-100" enter-from-class="transform opacity-0 scale-95" enter-to-class="transform opacity-100 scale-100" leave-active-class="transition ease-in duration-75" leave-from-class="transform opacity-100 scale-100" leave-to-class="transform opacity-0 scale-95">
        <MenuItems class="absolute left-0 z-100 mt-12 min-w-max origin-top-right rounded-md bg-white py-1 shadow-lg ring-1 ring-black ring-opacity-5 focus:outline-none">
          <MenuItem v-for="item in items" :key="item" v-slot="{ active }">
            <a :href="item.href" :class="[active ? 'bg-gray-100' : '', 'block px-4 py-2 text-sm text-gray-700']">{{ item.title }}</a>
          </MenuItem>
        </MenuItems>
      </transition>
    </Menu>
  </div>
</template>

<script setup>
import { Disclosure, DisclosureButton, DisclosurePanel, Menu, MenuButton, MenuItem, MenuItems } from '@headlessui/vue'

const props = defineProps({
  title: { type: String, required: true},
  href:  { type: String, default: undefined},
  items: { type: Array, default: []},
})
</script>