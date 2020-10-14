<template>
  <section class="testimonials-one">
    <div class="container">
      <div class="block-title text-center">
        <h2 class="block-title__title">What Our <span>Clients</span> Say <br> About Us.</h2><!-- /.block-title__title -->
      </div><!-- /.block-title -->
      <div class="testimonials-one__carousel-outer">
        <div class="testimonials-one__carousel owl-carousel owl-theme">
          <div class="item">
            <div class="testimonials-one__single">
              <div class="testimonials-one__inner">
                <p>This is due to their excellent service, competitive pricing and <br> customer support. It’s throughly refresing to get such a personal <br> touch. Duis aute irure dolor in reprehenderit.</p>
                <h3>Shirley Smith</h3>
                <span>Our Customers</span>
                <img src="/assets/images/resources/testi-1-1.png" alt="Awesome Image" />
              </div><!-- /.testimonials-one__inner -->
            </div><!-- /.testimonials-one__single -->
          </div><!-- /.item -->
          <div class="item">
            <div class="testimonials-one__single">
              <div class="testimonials-one__inner">
                <p>This is due to their excellent service, competitive pricing and <br> customer support. It’s throughly refresing to get such a personal <br> touch. Duis aute irure dolor in reprehenderit.</p>
                <h3>Shirley Smith</h3>
                <span>Our Customers</span>
                <img src="/assets/images/resources/testi-1-1.png" alt="Awesome Image" />
              </div><!-- /.testimonials-one__inner -->
            </div><!-- /.testimonials-one__single -->
          </div><!-- /.item -->
          <div class="item">
            <div class="testimonials-one__single">
              <div class="testimonials-one__inner">
                <p>This is due to their excellent service, competitive pricing and <br> customer support. It’s throughly refresing to get such a personal <br> touch. Duis aute irure dolor in reprehenderit.</p>
                <h3>Shirley Smith</h3>
                <span>Our Customers</span>
                <img src="/assets/images/resources/testi-1-1.png" alt="Awesome Image" />
              </div><!-- /.testimonials-one__inner -->
            </div><!-- /.testimonials-one__single -->
          </div><!-- /.item -->
        </div><!-- /.testimonials-one__carousel -->
        <div class="testimonials-one__carousel__shape-one"></div><!-- /.testimonials-one__carousel__shape-one -->
        <div class="testimonials-one__carousel__shape-two"></div><!-- /.testimonials-one__carousel__shape-two -->
        <div class="testimonials-one__nav">
          <a class="testimonials-one__nav-left" href="#"><i class="dimon-icon-left-arrow"></i></a>
          <a class="testimonials-one__nav-right" href="#"><i class="dimon-icon-right-arrow"></i></a>
        </div><!-- /.testimonials-one__nav -->
      </div><!-- /.testimonials-one__carousel-outer -->
    </div><!-- /.container -->
  </section>
</template>

<script>
    export default {
      name: "Testimonial",
      mounted() {
        if ($('.testimonials-one__carousel').length) {
          $('.testimonials-one__carousel').owlCarousel({
            loop: true,
            margin: 0,
            nav: false,
            dots: false,
            autoWidth: false,
            autoplay: true,
            smartSpeed: 700,
            autoplayTimeout: 5000,
            autoplayHoverPause: true,
            items: 1
          });

          $('.testimonials-one__nav-left').on('click', function() {
            $('.testimonials-one__carousel').trigger('next.owl.carousel');
            return false;
          });
          $('.testimonials-one__nav-right').on('click', function() {
            $('.testimonials-one__carousel').trigger('prev.owl.carousel');
            return false;
          });
        }
      }
    }
</script>

<style scoped>

</style>
