<template>
  <div>
    <footer class="site-footer">
      <div class="site-footer__upper">
        <div class="container">
          <div class="row">
            <div class="col-lg-3">
              <div class="footer-widget footer-widget__about">
                <img src="/assets/images/resources/logo-dark.png" width="119" alt="" class="footer-widget__logo">
                <p class="footer-widget__contact"><a href="tel:888-666-0000">888 666 0000</a></p>
                <!-- /.footer-widget__contact -->
                <p class="footer-widget__contact"><a href="mailto:needhelp@example.com">needhelp@example.com</a>
                <p class="footer-widget__contact">855 road, broklyn street <br> new york 600</p><!-- /.footer-widget__contact -->
              </div><!-- /.footer-widget -->
            </div><!-- /.col-lg-2 -->
            <div class="col-lg-6 d-flex justify-content-between footer-widget__links-wrap">
              <div class="footer-widget">
                <h3 class="footer-widget__title">Explore</h3><!-- /.footer-widget__title -->
                <ul class="footer-widget__links list-unstyled">
                  <li><a href="#">About</a></li>
                  <li><a href="#">Our Team</a></li>
                  <li><a href="#">Features</a></li>
                  <li><a href="#">Blog</a></li>
                  <li><a href="#">How It Works</a></li>
                </ul><!-- /.footer-widget__links -->
              </div><!-- /.footer-widget -->
              <div class="footer-widget">
                <h3 class="footer-widget__title">Services</h3><!-- /.footer-widget__title -->
                <ul class="footer-widget__links list-unstyled">
                  <li><a href="#">Speed Optimization </a></li>
                  <li><a href="#">Marketing Analysis </a></li>
                  <li><a href="#">SEO and Backlinks </a></li>
                  <li><a href="#">Content Marketing</a></li>
                </ul><!-- /.footer-widget__links -->
              </div><!-- /.footer-widget -->
              <div class="footer-widget">
                <h3 class="footer-widget__title">Links</h3><!-- /.footer-widget__title -->
                <ul class="footer-widget__links list-unstyled">
                  <li><a href="#">Help </a></li>
                  <li><a href="#">Support </a></li>
                  <li><a href="#">Clients </a></li>
                  <li><a href="#">Contact</a></li>
                </ul><!-- /.footer-widget__links -->
              </div><!-- /.footer-widget -->
            </div><!-- /.col-lg-6 -->
            <div class="col-lg-3">
              <div class="footer-widget">
                <div class="site-footer__social">
                  <a href="#" class="fa fa-facebook-square"></a>
                  <a href="#" class="fa fa-twitter"></a>
                  <a href="#" class="fa fa-instagram"></a>
                  <a href="#" class="fa fa-pinterest-p"></a>
                </div><!-- /.site-footer__social -->
              </div><!-- /.footer-widget -->
            </div><!-- /.col-lg-4 -->
          </div><!-- /.row -->
        </div><!-- /.container -->
      </div><!-- /.site-footer__upper -->
      <div class="site-footer__bottom">
        <div class="container">
          <div class="inner-container text-center">
            <p class="site-footer__copy">&copy; copyright 2020 by <a href="#">Layerdrops.com</a></p>
            <!-- /.site-footer__copy -->
          </div><!-- /.inner-container -->
        </div><!-- /.container -->
      </div><!-- /.site-footer__bottom -->
    </footer>

      <a href="#" data-target="html" class="scroll-to-target scroll-to-top"><i class="fa fa-angle-up"></i></a>

  </div>
</template>

<script>
    export default {
      name: "Footer",
      mounted() {

        $(window).on('scroll', function () {
          if ($('.scroll-to-top').length) {
            var strickyScrollPos = 100;
            if ($(window).scrollTop() > strickyScrollPos) {
              $('.scroll-to-top').fadeIn(500);
            } else if ($(this).scrollTop() <= strickyScrollPos) {
              $('.scroll-to-top').fadeOut(500);
            }
          }
        })
      }
    }
</script>

<style scoped>

</style>
