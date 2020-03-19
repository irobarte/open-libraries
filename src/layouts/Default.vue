<template>
  <div>
    <div class="flex flex-col relative">
      <HeaderPartial/>

      <main class="main inner flex flex-col py-10 lg:py-20 min-h-screen">
        <slot/>
      </main>

      <FooterPartial/>
    </div>
  </div>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<script>
import HeaderPartial from '~/layouts/partials/Header.vue'
import FooterPartial from '~/layouts/partials/Footer.vue'

export default {
  components: {
    HeaderPartial,
    FooterPartial
  }
}
</script>