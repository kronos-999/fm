<template>
  <div class="contents">
    <Navbar />
    <RouterView v-slot="{ Component }">
      <template v-if="Component">
        <Transition mode="out-in">
          <KeepAlive>
            <Suspense>
              <!-- main content -->
              <component :is="Component"></component>

              <!-- loading state -->
              <template #fallback>
                Loading...
              </template>
            </Suspense>
          </KeepAlive>
        </Transition>
      </template>
    </RouterView>
     <CTA
      header_1="Sie möchten einen Beitrag einreichen?"
      header_2="Schreiben Sie uns gerne Ihre Ideen"
      body="Sowohl unser Blog als auch unsere Zeitschrift 'Humanität' freut sich über kreative Ideen innerhalb der Freimaurerei."
      primary_btn_text="Jetzt Ideen einreichen"
      secondary_btn_text="Mehr erfahren"
      primary_btn_link=""
      secondary_btn_link=""
      />
    <Footer />
  </div>
</template>