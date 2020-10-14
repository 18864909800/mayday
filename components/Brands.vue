<template>
  <div class="brand-one">
    <div class="container">
      <div class="brand-one__carousel owl-carousel owl-theme">
        <div class="item">
          <img src="/assets/images/resources/brand-1-1.png" alt="">
        </div><!-- /.item -->
        <div class="item">
          <img src="/assets/images/resources/brand-1-1.png" alt="">
        </div><!-- /.item -->
        <div class="item">
          <img src="/assets/images/resources/brand-1-1.png" alt="">
        </div><!-- /.item -->
        <div class="item">
          <img src="/assets/images/resources/brand-1-1.png" alt="">
        </div><!-- /.item -->
        <div class="item">
          <img src="/assets/images/resources/brand-1-1.png" alt="">
        </div><!-- /.item -->
        <div class="item">
          <img src="/assets/images/resources/brand-1-1.png" alt="">
        </div><!-- /.item -->
        <div class="item">
          <img src="/assets/images/resources/brand-1-1.png" alt="">
        </div><!-- /.item -->
        <div class="item">
          <img src="/assets/images/resources/brand-1-1.png" alt="">
        </div><!-- /.item -->
        <div class="item">
          <img src="/assets/images/resources/brand-1-1.png" alt="">
        </div><!-- /.item -->
        <div class="item">
          <img src="/assets/images/resources/brand-1-1.png" alt="">
        </div><!-- /.item -->
        <div class="item">
          <img src="/assets/images/resources/brand-1-1.png" alt="">
        </div><!-- /.item -->
        <div class="item">
          <img src="/assets/images/resources/brand-1-1.png" alt="">
        </div><!-- /.item -->
      </div><!-- /.brand-one__carousel owl-carousel owl-theme -->
    </div><!-- /.container -->
  </div>
</template>

<script>
    export default {
      name: "Brands",
      mounted() {
        if ($('.brand-one__carousel').length) {
          $('.brand-one__carousel').owlCarousel({
            loop: true,
            margin: 115,
            nav: false,
            dots: false,
            autoWidth: false,
            autoplay: true,
            smartSpeed: 700,
            autoplayTimeout: 5000,
            autoplayHoverPause: true,
            responsive: {
              0: {
                items: 2,
                margin: 30
              },
              480: {
                items: 3,
                margin: 30
              },
              600: {
                items: 3,
                margin: 30
              },
              991: {
                items: 5,
                margin: 30
              },
              1000: {
                items: 5
              },
              1200: {
                items: 5
              }
            }
          });
        }
      }
    }
</script>

<style scoped>

</style>
