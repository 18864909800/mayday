<template>
  <div class="preloader">
    <img src="/assets/images/resources/preloader.png" class="preloader__image" alt="">
  </div>
</template>

<script>
    export default {
      name: "Preloader",
      mounted() {
          if ($('.preloader').length) {
            $('.preloader').fadeOut();
          }
      }
    }
</script>

<style scoped>

</style>
