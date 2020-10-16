<template>
  <section class="testimonials-one" id="testimonial">
    <div class="container">
      <div class="block-title text-center">
        <h2 class="block-title__title">五月天<span>团员</span> 介绍 <br> </h2><!-- /.block-title__title -->
      </div><!-- /.block-title -->
      <div class="testimonials-one__carousel-outer">
        <div class="testimonials-one__carousel owl-carousel owl-theme">
          <div class="item">
            <div class="testimonials-one__single">
              <div class="testimonials-one__inner">
                <p>1975年12月6日生于台北市北投区，中国台湾男歌手、词曲创作人，中国台湾摇滚乐团五月天的主唱，创意潮牌STAYREAL总裁。 <br> </p>
                <h3>陈信宏</h3>
                <span>主唱</span>
                <img src="/assets/images/resources/ashin.jpg" alt="Awesome Image" />
              </div><!-- /.testimonials-one__inner -->
            </div><!-- /.testimonials-one__single -->
          </div><!-- /.item -->
          <div class="item">
            <div class="testimonials-one__single">
              <div class="testimonials-one__inner">
                <p>1976年11月28日出生于中国台湾新竹市，五月天团长兼吉他手、作曲人、演员。毕业于台北师大附中、国立台湾大学社会系肄业。 <br> <br></p>
                <h3>怪兽</h3>
                <span>团长</span>
                <img src="/assets/images/resources/monster.jpg" alt="Awesome Image" />
              </div><!-- /.testimonials-one__inner -->
            </div><!-- /.testimonials-one__single -->
          </div><!-- /.item -->
          <div class="item">
            <div class="testimonials-one__single">
              <div class="testimonials-one__inner">
                <p>1977年4月25日出生于中国台湾高雄市，是乐团五月天的贝斯手、作曲人，毕业于台北师大附中、辅仁大学社会系肄业。任陶晶莹经营网站《姊妹淘》之专栏作家。 <br> <br> </p>
                <h3>玛莎</h3>
                <span>贝斯手</span>
                <img src="/assets/images/resources/MatthewTsai.jpg" alt="Awesome Image" />
              </div><!-- /.testimonials-one__inner -->
            </div><!-- /.testimonials-one__single -->
          </div><!-- /.item -->
          <div class="item">
            <div class="testimonials-one__single">
              <div class="testimonials-one__inner">
                <p>1975年12月11日生于中国台湾台北市，五月天吉他手，也是一名作曲人、演员，毕业于师大附中、淡江大学水环系肄业。主要作品有《如烟》、《仓颉》等。<br> <br></p>
                <h3>石头</h3>
                <span>吉他手</span>
                <img src="/assets/images/resources/stone.jpg" alt="Awesome Image" />
              </div><!-- /.testimonials-one__inner -->
            </div><!-- /.testimonials-one__single -->
          </div><!-- /.item -->
          <div class="item">
            <div class="testimonials-one__single">
              <div class="testimonials-one__inner">
                <p>1973年7月28日生于台湾苗栗，中国台湾摇滚乐团五月天的鼓手。1999年加入五月天乐团，担任鼓手。现有两个女儿，小玫瑰和小蔷薇，一家人幸福甜蜜。<br> <br></p>
                <h3>冠佑</h3>
                <span>鼓手</span>
                <img src="/assets/images/resources/lauming.jpg" alt="Awesome Image" />
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
