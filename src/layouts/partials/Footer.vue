<template>
  <div class="footer-wrapper">
    <footer id="footer" class="footer bg-gray-200" role="contentinfo">
      <div class="footer-inner container m-auto md:flex justify-between items-center px-6 py-10">
        <p class="text-purple-900 pb-8 md:pb-0">
          Template by
          <a href="https://github.com/josephdyer" target="_blank">Joseph Dyer</a>
          built with
          <a href="https://www.gridsome.org">Gridsome.</a>
        </p>

        <p class="text-purple-900">Last updated: March 19, 2020</p>
      </div>
    </footer>
  </div>
</template>

<script>
export default {}
</script>

<static-query>
query {
  metadata {
    social {
      icon
      link
    }
  }
}
</static-query>