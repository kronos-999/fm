<template>
  <Disclosure as="nav" class="bg-gray-800" v-slot="{ open }">
    <div class="mx-auto max-w-7xl px-2 sm:px-6 lg:px-8">
      <div class="relative flex h-16 items-center justify-between">
        <div class="absolute inset-y-0 right-0 flex items-center lg:hidden">
          <!-- Mobile menu button-->
          <DisclosureButton
            class="inline-flex items-center justify-center rounded-md p-2 text-gray-400 hover:bg-gray-700 hover:text-white focus:outline-none focus:ring-2 focus:ring-inset focus:ring-white">
            <span class="sr-only">Open main menu</span>
            <Bars3BottomRightIcon v-if="!open" class="block h-6 w-6" aria-hidden="true" />
            <XMarkIcon v-else class="block h-6 w-6" aria-hidden="true" />
          </DisclosureButton>
        </div>
        <div class="flex flex-1 items-center justify-center sm:items-stretch sm:justify-start">
          <div class="flex flex-shrink-0 items-center">
            <img class="brightness-200 block h-8 w-auto lg:hidden" src="/logo.png" />
            <img class="brightness-200 hidden h-8 w-auto lg:block" src="/logo.png" />
          </div>
          <div class="hidden sm:ml-6 lg:flex items-center">
            <div class="flex gap-x-4">
              <DropdownItem v-for="nav in navigation" :key="nav.title" :title="nav.title" :href="nav.href" :items="nav.items" />
            </div>
          </div>
        </div>
      </div>
    </div>

    <DisclosurePanel class="lg:hidden">
      <div class="px-2 pb-3 pt-2">
        <div class="my-3" v-for="nav in navigation" :key="nav.title">
          <a class="text-lg font-md" v-if="!!nav?.href" :href="nav?.href">
            {{ nav.title }}
          </a>
          <button type="button" class="text-lg font-md" @click="nav.isMobileOpen = !nav.isMobileOpen" v-else>
            <span class="flex items-center gap-x-2">
              {{ nav.title }}
              <ChevronDownIcon class="flex h-4 w-4" v-if="nav?.items?.length && nav.isMobileOpen == true" />
              <ChevronUpIcon   class="flex h-4 w-4" v-if="nav?.items?.length && nav.isMobileOpen == false" />
            </span>
          </button>
          <ul class="block" v-if="!nav?.href && nav?.items?.length && nav.isMobileOpen == true">
            <li class="ml-3" v-for="link in nav.items">
              <a class="text-sm font-md" :href="link.href">
                {{ link.title }}
              </a>
            </li>
          </ul>
        </div>
      </div>
  </DisclosurePanel>
</Disclosure></template>

<script setup>
import { Disclosure, DisclosureButton, DisclosurePanel, Menu, MenuButton, MenuItem, MenuItems } from '@headlessui/vue'
import { Bars3BottomRightIcon, XMarkIcon, ChevronDownIcon, ChevronUpIcon } from '@heroicons/vue/24/outline'

const navigation = reactive([
  {
    title: 'Start',
    href: '/',
  },
  {
    title: 'Informationen',
    href: '/',
  },
  {
    title: 'Blog',
    href: '/',
  },
  {
    title: 'Großloge',
    href: '/',
  },
  {
    title: 'Distrikte',
    isMobileOpen: false,
    items: [
      { title: "Baden-Württemberg", href: "#amk" },
      { title: "Bayern", href: "#" },
      { title: "Berlin / Brandenburg", href: "#" },
      { title: "Bremen", href: "#" },
      { title: "Hamburg", href: "#" },
      { title: "Hessen / Thüringen", href: "#" },
      { title: "Niedersachsen / Sachsen-Anhalt", href: "#" },
      { title: "Nordrhein-Westfalen", href: "#" },
      { title: "Rheinland-Pfalz / Saarland", href: "#" },
      { title: "Sachsen", href: "#" },
      { title: "Schleswig-Holstein / Mecklenburg-Vorpommern", href: "#" },
    ]
  },
  {
    title: 'Newsletter',
    href: '/',
  },
  {
    title: 'Mehr',
    href: '/',
  },
  {
    title: 'Suche',
    href: '/',
  },
  {
    title: 'Veranstaltungen',
    href: '/',
  },
])
</script>