<template>
  <section class="fact-one">
    <div class="container">
      <div class="block-title text-center">
        <h2 class="block-title__title">Over 2200 <span>Projects</span> <br> Completed.</h2><!-- /.block-title__title -->
      </div><!-- /.block-title -->
      <div class="row">
        <div class="col-lg-3 col-md-6 col-sm-12 wow fadeInUp" data-wow-duration="1500ms">
          <div class="fact-one__single">
            <div class="fact-one__inner">
              <h3 class="fact-one__count counter">4789</h3><!-- /.fact-one__count counter -->
              <p class="fact-one__text">projects</p><!-- /.fact-one__text -->
            </div><!-- /.fact-one__inner -->
          </div><!-- /.fact-one__single -->
        </div><!-- /.col-lg-3 col-md-6 col-sm-12 -->
        <div class="col-lg-3 col-md-6 col-sm-12 wow fadeInUp" data-wow-duration="1500ms">
          <div class="fact-one__single">
            <div class="fact-one__inner">
              <h3 class="fact-one__count counter">6400</h3><!-- /.fact-one__count counter -->
              <p class="fact-one__text">customers</p><!-- /.fact-one__text -->
            </div><!-- /.fact-one__inner -->
          </div><!-- /.fact-one__single -->
        </div><!-- /.col-lg-3 col-md-6 col-sm-12 -->
        <div class="col-lg-3 col-md-6 col-sm-12 wow fadeInUp" data-wow-duration="1500ms">
          <div class="fact-one__single">
            <div class="fact-one__inner">
              <h3 class="fact-one__count counter">960</h3><!-- /.fact-one__count counter -->
              <p class="fact-one__text">success</p><!-- /.fact-one__text -->
            </div><!-- /.fact-one__inner -->
          </div><!-- /.fact-one__single -->
        </div><!-- /.col-lg-3 col-md-6 col-sm-12 -->
        <div class="col-lg-3 col-md-6 col-sm-12 wow fadeInUp" data-wow-duration="1500ms">
          <div class="fact-one__single">
            <div class="fact-one__inner">
              <h3 class="fact-one__count counter">378</h3><!-- /.fact-one__count counter -->
              <p class="fact-one__text">awards</p><!-- /.fact-one__text -->
            </div><!-- /.fact-one__inner -->
          </div><!-- /.fact-one__single -->
        </div><!-- /.col-lg-3 col-md-6 col-sm-12 -->
      </div><!-- /.row -->
    </div><!-- /.container -->
  </section>
</template>

<script>
    export default {
      name: "Counter",
      mounted() {
        if ($('.counter').length) {
          $('.counter').counterUp({
            delay: 10,
            time: 3000
          });
        }
      }
    }
</script>

<style scoped>

</style>
