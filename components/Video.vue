<template>
  <section class="video-one" id="video">
    <img src="/assets/images/background/video-one-bg.png" alt="Awesome Image" class="video-one__bg" />
    <div class="container wow fadeInUp" data-wow-duration="1500ms">
      <div class="video-one__box ">
        <img src="/assets/images/resources/video-1-1.jpg" alt="">
        <div class="video-one__content">
          <a href="https://www.youtube.com/watch?v=coI_aT4BDNA" class="video-popup video-one__btn"><i class="fa fa-play"></i><!-- /.fa fa-play --></a>
          <!-- /.video-popup -->
          <h2 class="video-one__title">Watch Our <span>Tutorial</span> <br> Videos.</h2><!-- /.video-one__title -->
        </div><!-- /.video-one__content -->
      </div><!-- /.video-one__box -->
    </div><!-- /.container -->
  </section>
</template>

<script>
    export default {
      name: "Video",
      mounted() {
        if ($('.video-popup').length) {
          $('.video-popup').magnificPopup({
            disableOn: 700,
            type: 'iframe',
            mainClass: 'mfp-fade',
            removalDelay: 160,
            preloader: true,

            fixedContentPos: false
          });
        }
      }
    }
</script>

<style scoped>

</style>
