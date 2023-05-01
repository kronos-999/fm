<template>
  <div class="relative isolate overflow-hidden bg-white px-6 py-24 sm:py-32 lg:overflow-visible lg:px-0">
    <div class="absolute inset-0 -z-10 overflow-hidden">
      <svg
        class="absolute left-[max(50%,25rem)] top-0 h-[64rem] w-[128rem] -translate-x-1/2 stroke-gray-200 [mask-image:radial-gradient(64rem_64rem_at_top,white,transparent)]"
        aria-hidden="true">
        <defs>
          <pattern id="e813992c-7d03-4cc4-a2bd-151760b470a0" width="200" height="200" x="50%" y="-1"
            patternUnits="userSpaceOnUse">
            <path d="M100 200V.5M.5 .5H200" fill="none" />
          </pattern>
        </defs>
        <svg x="50%" y="-1" class="overflow-visible fill-gray-50">
          <path d="M-100.5 0h201v201h-201Z M699.5 0h201v201h-201Z M499.5 400h201v201h-201Z M-300.5 600h201v201h-201Z"
            stroke-width="0" />
        </svg>
        <rect width="100%" height="100%" stroke-width="0" fill="url(#e813992c-7d03-4cc4-a2bd-151760b470a0)" />
      </svg>
    </div>
    <div
      class="mx-auto grid max-w-2xl grid-cols-1 gap-x-8 gap-y-16 lg:mx-0 lg:max-w-none lg:grid-cols-2 lg:items-start lg:gap-y-10">
      <div
        class="lg:col-span-2 lg:col-start-1 lg:row-start-1 lg:mx-auto lg:grid lg:w-full lg:max-w-7xl lg:grid-cols-2 lg:gap-x-8 lg:px-8">
        <div class="lg:pr-4">
          <div class="lg:max-w-lg">
            <p class="text-base font-semibold leading-7 text-indigo-600">DISTRIKT HESSEN / THÜRINGEN</p>
            <h1 class="mt-2 text-3xl font-bold tracking-tight text-gray-900 sm:text-4xl">175-Jahrfeier Frankfurter Pauls­kirchen­parlament</h1>
            <p class="mt-6 text-xl leading-8 text-gray-700">
              Das Paulskirchenparlament von 1848 gilt als Wiege der deutschen Demokratie und hat einen engen freimaurerischen Bezug.
            </p>
          </div>
        </div>
      </div>
      <div class="-ml-12 -mt-12 p-12 lg:sticky lg:top-4 lg:col-start-2 lg:row-span-2 lg:row-start-1 lg:overflow-hidden">
        <img class="w-[48rem] max-w-none rounded-xl bg-gray-900 shadow-xl ring-1 ring-gray-400/10 sm:w-[57rem]"
          src="https://www.freimaurerei.de/wp-content/uploads/2023/04/AdobeStock_216408385.jpeg" alt="" />
        <span class="text-gray-700 ml-1">
          Innenansicht der Frankfurter Paulskirche (Foto: Matthias / stock.adobe.com)
        </span>
      </div>
      <div
        class="lg:col-span-2 lg:col-start-1 lg:row-start-2 lg:mx-auto lg:grid lg:w-full lg:max-w-7xl lg:grid-cols-2 lg:gap-x-8 lg:px-8">
        <div class="lg:pr-4">
          <div class="max-w-xl text-base leading-7 text-gray-700 lg:max-w-lg">
            <p class="my-3">
             Der “Deutschen Nationalversammlung” vorausgegangen war eine revolutionäre Welle in ganz Europa, deren Grund in wirtschaftlichen Krisen, Massenarmut und allgemeiner politischer Unzufriedenheit zu suchen war. Auch in Deutschland wurden mehr Grund- und Freiheitsrechte gefordert. In der Folge wurde die Zensur aufgehoben, es wurden politische Aktivitäten gestattet und weitere Zugeständnisse gemacht. Am 18. Mai 1848 versammelten sich in der Frankfurter Paulskirche Mitglieder eines ersten gesamtdeutschen Parlaments. Ziel waren Beratungen über eine freiheitliche Verfassung und die Bildung eines Nationalstaates.
            </p>
            <p class="my-3">
              Durch das in der Frankfurter Nationalversammlung verabschiedete “Reichsgesetz betreffend die Grundrechte des deutschen Volkes” erlangten erstmals Menschen- und Bürgerrechte in Deutschland Gesetzeskraft. Grundelemente waren die Gleichheit vor dem Gesetz, Aufhebung der Standesvorrechte, persönliche und politische Freiheitsrechte wie Presse-, Meinungs-, Versammlungs- und Gewerbefreiheit sowie die Abschaffung der Todesstrafe.
              Ungefähr zehn Prozent der Parlamentarier im Jahr 1848 waren Freimaurer. Sie vertraten unterschiedliche politische Überzeugungen. Das erfüllt uns heute noch mit Stolz, ist es doch Teil der freimaurerischen DNA, über politische und religiöse Strömungen hinweg das Gespräch und den geistigen Austausch zu suchen. Wir möchten diese Jubiläums-Veranstaltungen entsprechend dazu nutzen, um auch ausgewählte, nicht freimaurerische Gäste einzuladen, und so ein Stück Freimaurerei in die Öffentlichkeit zu tragen.
            </p>
            <p class="my-3">
              Aus diesem Anlass laden die Logen des Frankfurter Meisterzirkels unter der Schirmherrschaft des ehrwürdigsten Großmeisters der Vereinigten Großlogen von Deutschland, Br. Michael Volkwein, herzlich ein, dieses Jubiläum gemeinsam zu begehen.
            </p>

            <Table :items="schedule_1" header="Programm Festakt am Freitag, dem 26. Mai 2023" />
            <Table :items="schedule_2" header="Weiße Arbeit am Samstag, dem 27. Mai 2023" />

            <ul role="list" class="mt-8 space-y-8 text-gray-600">
              <li class="flex gap-x-3">
                <EnvelopeIcon class="mt-1 h-5 w-5 flex-none text-indigo-600" aria-hidden="true" />
                <span>
                  <strong class="font-semibold text-gray-900">Teilnahme</strong> <br />
                  Ausrichter ist der Frankfurter Meisterzirkel. Weitere Informationen über die E-Mail-Adresse info@freimaurer-frankfurt.de. Anmeldungen über den Link https://app.guestoo.de/public/event/a4e6b104-7698-4f55-a3d1-b189847f43ea
                </span>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { EnvelopeIcon } from '@heroicons/vue/24/outline'
const schedule_1 = [
  {
    title: 'Sektempfang',
    subitems: [
      { title: "", subtitle: "Begrüßung durch das Organisationskomitee des Frankfurter Meisterzirkels"}
    ]
  },
  {
    title: 'Grußworte',
    subitems: [
      { title: "Michael Volkwein",     subtitle: "Großmeister der Vereinigten Großlogen von Deutschland" },
      { title: "Stefan Kunnert",       subtitle: "Großmeister der Großloge der Alten Freien und Angenommenen Maurer von Deutschland" },
      { title: "Franka Drewies-Lahrs", subtitle: "Großmeisterin der Frauengroßloge von Deutschland" },
    ]
  },
  {
    title: 'Festvortrag',
    subitems: [
      { title: "Thomas Forwe",                               subtitle: "Zugeordneter Großmeister der Alten Freien und Angenommenen Maurer von Deutschland" },
      { title: "„Die Paulskirche als Wiege der Demokratie“", subtitle: "" },
    ]
  },
  {
    title: 'Festbankett',
    subitems: [
      { title: "", subtitle: "Musikalische Begleitung durch Schwestern und Brüder des Frankfurter Meisterzirkels "}
    ]
  },
]

const schedule_2 = [
  {
    title: 'Kleiderordnung',
    subitems: [
      { title: "", subtitle: "Brr./Srr. Freimaurer: dunkler Anzug, weißer Binder, Bijou; Begleitung gedeckt." },
      { title: "", subtitle: "Einlass ab 16:00 Uhr, Beginn 17:00 Uhr. Im Anschluss findet ein gemeinsamer Imbiss statt. " },
    ]
  },
  {
    title: 'Grußworte',
    subitems: [
      { title: "Michael Volkwein",     subtitle: "Großmeister der Vereinigten Großlogen von Deutschland" },
      { title: "Stefan Kunnert",       subtitle: "Großmeister der Großloge der Alten Freien und Angenommenen Maurer von Deutschland" },
      { title: "Franka Drewies-Lahrs", subtitle: "Großmeisterin der Frauengroßloge von Deutschland" },
    ]
  },
  {
    title: 'Zeichnung',
    subitems: [
      { title: "Wolfgang Böhm", subtitle: "Großredner der Großloge der Alten Freien und Angenommenen Maurer von Deutschland" }
    ]
  },
  {
    title: '',
    subitems: [
      { title: "", subtitle: "Musikalische Begleitung durch Schwestern und Brüder des Frankfurter Meisterzirkels " }
    ]
  },
]
</script>

<route lang="yaml">
meta:
  layout: post
</route>
