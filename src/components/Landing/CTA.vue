<!-- This example requires Tailwind CSS v3.0+ -->
<template>
  <div class="bg-white">
    <div class="py-24 px-6 sm:px-6 sm:py-32 lg:px-8">
      <div class="mx-auto max-w-2xl text-center">
        <h2 class="text-4xl font-bold tracking-tight text-gray-900">
        {{ header_1 }}
        <br />
        {{ header_2 }}
        </h2>
        <p class="mx-auto mt-6 max-w-xl text-lg leading-8 text-gray-600">
          {{ body }}
        </p>
        <div class="mt-10 flex items-center justify-center gap-x-6">
          <a :href="primary_btn_link" class="rounded-md bg-indigo-600 px-3.5 py-1.5 text-base font-semibold leading-7 text-white shadow-sm hover:bg-indigo-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600">
            {{ primary_btn_text }}
          </a>
          <a :href="secondary_btn_link" class="text-base font-semibold leading-7 text-gray-900">
            {{ secondary_btn_text }}
            <span aria-hidden="true">→</span>
          </a>
        </div>
      </div>
  </div>
</div>
</template>

<script setup>
const props = defineProps({
  header_1:           String,
  header_2:           String,
  body:               String,
  primary_btn_text:   String,
  secondary_btn_text: String,
  primary_btn_link:   String,
  secondary_btn_link: String,
})
</script>
