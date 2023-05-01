<!-- This example requires Tailwind CSS v2.0+ -->
<template>
  <div class="relative bg-white pt-16 pb-20 px-4 sm:px-6 lg:pt-24 lg:pb-28 lg:px-8">
    <div class="absolute inset-0">
      <div class="bg-white h-1/3 sm:h-2/3" />
    </div>
    <div class="relative max-w-7xl mx-auto">
      <div class="text-center">
        <h2 class="text-3xl tracking-tight font-extrabold text-gray-900 sm:text-4xl">
          AFuAMvD Blog
        </h2>
        <p class="mt-3 max-w-2xl mx-auto text-xl text-gray-500 sm:mt-4">
          Herzlich willkommen in unserem Blog! Hier finden Sie alle Informationen zu unseren neuesten Events, Mitgliedern und anderen aufregenden Neuheiten. Wir sind stolz darauf, Ihnen einen Einblick in unsere Gemeinschaft zu geben und Ihnen zu zeigen, was wir alles zu bieten haben. Ob Sie ein langjähriges Mitglied sind oder uns gerade erst entdeckt haben, hier finden Sie alles, was Sie wissen müssen. Schauen Sie also regelmäßig vorbei, um auf dem Laufenden zu bleiben!
        </p>
      </div>
      <div class="mt-12 max-w-lg mx-auto grid gap-5 lg:grid-cols-3 lg:max-w-none">
        <div v-for="post in posts" :key="post.title" class="flex flex-col rounded-lg shadow-lg overflow-hidden">
          <div class="flex-shrink-0">
            <img class="h-48 w-full object-cover" :src="post.imageUrl" alt="" />
          </div>
          <div class="flex-1 bg-white p-6 flex flex-col justify-between">
            <div class="flex-1">
              <p class="text-sm font-medium text-indigo-600">
                <a :href="post.href" class="hover:underline">
                  {{ post.category.name }}
                </a>
              </p>
              <a :href="post.href" class="block mt-2">
                <p class="text-xl font-semibold text-gray-900">
                  {{ post.title }}
                </p>
                <p class="mt-3 text-base text-gray-500">
                  {{ post.description }}
                </p>
              </a>
            </div>
            <div class="mt-6 flex items-center">
              <div class="w-full">
                <div class="w-full flex items-center justify-between space-x-1 text-sm text-gray-500">
                  <div class="">
                    <time :datetime="post.datetime">
                      {{ post.date }}
                    </time>
                    <span aria-hidden="true">
                      &middot;
                    </span>
                    <span> {{ post.readingTime }} Lesezeit </span>
                  </div>

                  <a :href="post.href" class="rounded-md bg-indigo-600 px-2 py-1 text-base font-semibold leading-7 text-white shadow-sm hover:bg-indigo-700 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-400">
                    Weiterlesen
                  </a>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const posts = [
  {
    title: 'Masonicum in Walkenried',
    href: '/1',
    category: { name: 'DISTRIKT NIEDERSACHSEN / SACHSEN-ANHALT', href: '#' },
    description: 'Zum 40. Mal treffen sich Freimaurer und seit einigen Jahren auch Freimaurerinnen im Harz zu einem Masonicum.',
    date: '27. April 2023',
    datetime: '2023-04-27',
    imageUrl: 'https://www.freimaurerei.de/wp-content/uploads/2023/04/AdobeStock_403005152.jpeg',
    readingTime: '6 Min',
  },
  {
    title: '175-Jahrfeier Frankfurter Pauls­kirchen­parlament',
    href: '/2',
    category: { name: 'DISTRIKT HESSEN / THÜRINGEN', href: '#' },
    description: 'Das Paulskirchenparlament von 1848 gilt als Wiege der deutschen Demokratie und hat einen engen freimaurerischen Bezug.',
    date: '27. April 2023',
    datetime: '2023-04-27',
    imageUrl: 'https://www.freimaurerei.de/wp-content/uploads/2023/04/AdobeStock_216408385.jpeg',
    readingTime: '4 Min',
  },
  {
    title: "Jahresbeginnfeier der Loge 'Eleusis zur Verschwiegenheit'",
    href: '/3',
    category: { name: 'DISTRIKT BAYERN', href: '#' },
    description: "Guter Tradition entsprechend, haben die Brüder und Schwestern der Bayreuther Loge „Eleusis zur Verschwiegenheit“ auch das Jahr 2023 mit einer künstlerischen Darbietung begonnen.",
    date: '13. April 2023',
    datetime: '2023-04-13',
    imageUrl: 'https://www.freimaurerei.de/wp-content/uploads/2023/04/20230107_183735.jpg.webp',
    readingTime: '11 Min',
  },
]
</script>