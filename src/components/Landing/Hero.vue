<!-- This example requires Tailwind CSS v3.0+ -->
<template>
  <div class="relative isolate overflow-hidden bg-gray-900">
    <img
      src="https://images.unsplash.com/photo-1682176162464-3a11b5ea3774?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1174&q=80"
      alt="" class="opacity-30 absolute inset-0 -z-10 h-full w-full object-cover" />
    <div class="absolute inset-x-0 top-[-10rem] -z-10 transform-gpu overflow-hidden blur-3xl sm:top-[-20rem]">
      <svg
        class="relative left-[calc(50%-11rem)] -z-10 h-[21.1875rem] max-w-none -translate-x-1/2 rotate-[30deg] sm:left-[calc(50%-30rem)] sm:h-[42.375rem]"
        viewBox="0 0 1155 678">
        <path fill="url(#45de2b6b-92d5-4d68-a6a0-9b9b2abad533)" fill-opacity=".2"
          d="M317.219 518.975L203.852 678 0 438.341l317.219 80.634 204.172-286.402c1.307 132.337 45.083 346.658 209.733 145.248C936.936 126.058 882.053-94.234 1031.02 41.331c119.18 108.451 130.68 295.337 121.53 375.223L855 299l21.173 362.054-558.954-142.079z" />
        <defs>
          <linearGradient id="45de2b6b-92d5-4d68-a6a0-9b9b2abad533" x1="1155.49" x2="-78.208" y1=".177" y2="474.645"
            gradientUnits="userSpaceOnUse">
            <stop stop-color="#9089FC" />
            <stop offset="1" stop-color="#FF80B5" />
          </linearGradient>
        </defs>
      </svg>
    </div>
    <div class="px-6 lg:px-8">
      <nav class="flex items-center justify-between pt-6" aria-label="Global">
        <div class="flex lg:flex-1">
          <a href="#" class="-m-1.5 p-1.5">
            <span class="sr-only">Your Company</span>
            <img class="brightness-200 opacity-100 h-18 w-auto" src="/logo.png" alt="" />
          </a>
        </div>
        <div class="flex md:hidden">
          <a href="#" class="text-xl font-semibold leading-6 text-white">AFuAMvD</a>
        </div>
        <div class="flex lg:hidden">
          <button type="button" class="-m-2.5 inline-flex items-center justify-center rounded-md p-2.5 text-gray-400"
            @click="mobileMenuOpen = true">
            <span class="sr-only">Open main menu</span>
            <Bars3BottomRightIcon class="h-6 w-6" aria-hidden="true" />
          </button>
        </div>
        <div class="hidden lg:flex lg:gap-x-12">
          <a v-for="item in navigation" :key="item.name" :href="item.href"
            class="text-sm font-semibold leading-6 text-white">{{ item.name }}</a>
          <!-- <FlyoutMenuSingle /> -->
        </div>
        <div class="hidden lg:flex lg:flex-1 lg:justify-end">
          <!-- <a href="#" class="text-sm font-semibold leading-6 text-white">Log in <span aria-hidden="true">&rarr;</span></a> -->
        </div>
      </nav>
      <Dialog as="div" @close="mobileMenuOpen = false" :open="mobileMenuOpen">
        <DialogPanel focus="true" class="fixed inset-0 z-10 overflow-y-auto bg-gray-900 px-6 py-6 lg:hidden">
          <div class="flex items-center justify-between">
            <a href="#" class="-m-1.5 p-1.5">
              <span class="sr-only">Your Company</span>
              <img class="brightness-200 opacity-100 h-18 w-auto" src="/logo.png" alt="" />
            </a>
            <button type="button" class="-m-2.5 rounded-md p-2.5 text-gray-400" @click="mobileMenuOpen = false">
              <span class="sr-only">Close menu</span>
              <XMarkIcon class="h-6 w-6" aria-hidden="true" />
            </button>
          </div>
          <div class="mt-6 flow-root">
            <div class="-my-6 divide-y divide-gray-500/25">
              <div class="space-y-2 py-6">
                <a v-for="item in navigation" :key="item.name" :href="item.href"
                  class="-mx-3 block rounded-lg py-2 px-3 text-base font-semibold leading-7 text-white hover:bg-gray-400/10">{{ item.name }}</a>
                <!-- <FlyoutMenuSingle /> -->
              </div>
              <!-- <div class="py-6">
                <a href="#"
                  class="-mx-3 block rounded-lg py-2.5 px-3 text-base font-semibold leading-6 text-white hover:bg-gray-400/10">Log
                  in</a>
              </div> -->
            </div>
          </div>
        </DialogPanel>
      </Dialog>
      <div class="mx-auto max-w-2xl py-32 sm:py-48 lg:py-56">
        <div class="hidden sm:mb-8 sm:flex sm:justify-center">
          <div class="relative rounded-full py-1 px-3 text-sm leading-6 text-gray-100 ring-1 ring-white/10 hover:ring-white/20">
            Unsere Zeitschrift "Humanität" jetzt in digitaler Form erhältlich |
            <a href="#" class="font-semibold text-white">
              <span class="absolute inset-0" aria-hidden="true" />
              Mehr erfahren
              <span aria-hidden="true">&rarr;</span>
            </a>
          </div>
        </div>
        <div class="text-center">
          <h1 class="text-3xl font-semibold tracking-tight text-white sm:text-5xl">
            Großloge der Alten Freien und Angenommenen Maurer von Deutschland (AFuAMvD)
          </h1>
          <p class="mt-6 text-lg leading-8 text-gray-300">

          </p>
          <div class="mt-10 flex items-center justify-center gap-x-6">
            <a href="#about"
              class="w-1/2 rounded-md bg-indigo-600 px-3.5 py-1.5 text-base font-semibold leading-7 text-white shadow-sm hover:bg-indigo-700 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-400">
            Mehr erfahren
            </a>
           <!--  <a href="#" class="text-base font-semibold leading-7 text-white">Learn more <span
                aria-hidden="true">→</span></a> -->
          </div>
        </div>
      </div>
    </div>
    <div
      class="absolute inset-x-0 top-[calc(100%-13rem)] -z-10 transform-gpu overflow-hidden blur-3xl sm:top-[calc(100%-30rem)]">
      <svg
        class="relative left-[calc(50%+3rem)] h-[21.1875rem] max-w-none -translate-x-1/2 sm:left-[calc(50%+36rem)] sm:h-[42.375rem]"
        viewBox="0 0 1155 678">
        <path fill="url(#ecb5b0c9-546c-4772-8c71-4d3f06d544bc)" fill-opacity=".2"
          d="M317.219 518.975L203.852 678 0 438.341l317.219 80.634 204.172-286.402c1.307 132.337 45.083 346.658 209.733 145.248C936.936 126.058 882.053-94.234 1031.02 41.331c119.18 108.451 130.68 295.337 121.53 375.223L855 299l21.173 362.054-558.954-142.079z" />
        <defs>
          <linearGradient id="ecb5b0c9-546c-4772-8c71-4d3f06d544bc" x1="1155.49" x2="-78.208" y1=".177" y2="474.645"
            gradientUnits="userSpaceOnUse">
            <stop stop-color="#9089FC" />
            <stop offset="1" stop-color="#FF80B5" />
        </linearGradient>
      </defs>
    </svg>
  </div>
</div></template>

<script setup>
import { ref } from 'vue'
import { Dialog, DialogPanel } from '@headlessui/vue'
import { Bars3BottomRightIcon, XMarkIcon } from '@heroicons/vue/24/outline'

const navigation = [
  { name: 'Start',               href: '#' },
  { name: 'Informationen',       href: '#' },
  { name: 'Blog',          href: '#' },
  { name: 'Großloge',            href: '#' },
  { name: 'Distrikte',           href: '#' },
  { name: 'Newsletter',          href: '#newsletter' },
  { name: 'Mehr',                href: '#' },
  { name: 'Suche',               href: '#' },
  { name: 'Veranstaltungen',     href: '#' },
]

const mobileMenuOpen = ref(false)
</script>

<style>
* {
  scroll-behavior: smooth;
}
</style>