<template>
  <header class="site-header site-header__header-one site-header__header-two">
    <nav class="navbar navbar-expand-lg navbar-light header-navigation stricky">
      <div class="container clearfix">
        <!-- Brand and toggle get grouped for better mobile display -->
        <div class="logo-box clearfix">
          <a class="navbar-brand" href="/">
            <img src="/assets/images/resources/logo-light.png" class="main-logo" width="119" alt="Awesome Image" />
          </a>
          <button class="menu-toggler" data-target=".main-navigation">
            <span class="fa fa-bars"></span>
          </button>
        </div><!-- /.logo-box -->
        <!-- Collect the nav links, forms, and other content for toggling -->
        <div class="main-navigation">
          <ul class=" one-page-scroll-menu navigation-box">
            <li class="current scrollToLink">
              <a href="#">Home</a>
              <ul class="sub-menu">
                <li><a href="/">Home 01</a></li>
                <li><a href="/index-2">Home 02</a></li>
              </ul><!-- /.sub-menu -->
            </li>
            <li class="scrollToLink">
              <a href="#features">Features</a>

            </li>
            <li class="scrollToLink">
              <a href="#video">Video</a>

            </li>
            <li class="scrollToLink">
              <a href="#pricing">Pricing</a>
            </li>
            <li class="scrollToLink">
              <a href="#screenshots">App Screenshots</a>
            </li>
            <li class="scrollToLink">
              <a href="#news">News</a>
              <ul class="sub-menu">
                <li><nuxt-link to="/blog">News Page</nuxt-link></li>
                <li><nuxt-link to="/blog-details">News Details</nuxt-link></li>
              </ul><!-- /.sub-menu -->
            </li>
          </ul>
        </div><!-- /.navbar-collapse -->
        <div class="right-side-box">
          <a class="thm-btn header__cta-btn" href="#"><span>Login</span></a>
        </div><!-- /.right-side-box -->
      </div>
      <!-- /.container -->
    </nav>
  </header>
</template>

<script>
    export default {
      name: "Header",
      mounted() {

        // sticky menu
        $(window).on('scroll', function () {
          // checks if window is scrolled more than 500px, adds/removes solid class
          if ($(this).scrollTop() > 60) {
            $('.stricky').addClass('original');
            $('.stricky').addClass('stricked-menu');
          } else {
            $('.navbar').removeClass('original');
            $('.stricky').removeClass('stricked-menu');
          }
        });
        if ($('.main-navigation .navigation-box').length) {
          var subMenu = $('.main-navigation .sub-menu');
          subMenu.parent('li').children('a').append(function() {
            return '<button class="sub-nav-toggler"> <span class="sr-only">Toggle navigation</span> <span class="icon-bar"></span> <span class="icon-bar"></span> <span class="icon-bar"></span> </button>';
          });
          var mainNavToggler = $('.header-navigation .menu-toggler');
          var subNavToggler = $('.main-navigation .sub-nav-toggler');
          mainNavToggler.on('click', function() {
            var Self = $(this);
            var menu = Self.data('target');
            $(menu).slideToggle();
            $(menu).toggleClass('showen');
            return false;
          });
          subNavToggler.on('click', function() {
            var Self = $(this);
            Self.parent().parent().children('.sub-menu').slideToggle();
            return false;
          });
        }
        if ($('.scroll-to-target').length) {
          $(".scroll-to-target").on('click', function() {
            var target = $(this).attr('data-target');
            // animate
            $('html, body').animate({
              scrollTop: $(target).offset().top
            }, 1000);

            return false;

          });
        }
        function SmoothMenuScroll() {
          var anchor = $('.scrollToLink');
          if (anchor.length) {
            anchor.children('a').bind('click', function(event) {
              if ($(window).scrollTop() > 10) {
                var headerH = '67';
              } else {
                var headerH = '100';
              }
              var target = $(this);
              $('html, body').stop().animate({
                scrollTop: $(target.attr('href')).offset().top - headerH + 'px'
              }, 1200, 'easeInOutExpo');
              anchor.removeClass('current');
              target.parent().addClass('current');
              event.preventDefault();
            });
          }
        }
        SmoothMenuScroll();

        function OnePageMenuScroll() {
          var windscroll = $(window).scrollTop();
          if (windscroll >= 100) {
            var menuAnchor = $('.one-page-scroll-menu .scrollToLink').children('a');
            menuAnchor.each(function() {
              // grabing section id dynamically
              var sections = $(this).attr('href');
              $(sections).each(function() {
                // checking is scroll bar are in section
                if ($(this).offset().top <= windscroll + 100) {
                  // grabing the dynamic id of section
                  var Sectionid = $(sections).attr('id');
                  // removing current class from others
                  $('.one-page-scroll-menu').find('li').removeClass('current');
                  // adding current class to related navigation
                  $('.one-page-scroll-menu').find('a[href*=\\#' + Sectionid + ']').parent().addClass('current');
                }
              });
            });
          } else {
            $('.one-page-scroll-menu li.current').removeClass('current');
            $('.one-page-scroll-menu li:first').addClass('current');
          }
        }

        if ($('.side-menu__toggler').length) {
          $('.side-menu__toggler').on('click', function(e) {
            $('.side-menu__block').addClass('active');
            e.preventDefault();
          });
        }

        if ($('.side-menu__block-overlay').length) {
          $('.side-menu__block-overlay').on('click', function(e) {
            $('.side-menu__block').removeClass('active');
            e.preventDefault();
          });
        }

        $(window).on('scroll', function() {
          if ($('.stricked-menu').length) {
            var headerScrollPos = 100;
            var stricky = $('.stricked-menu');
            if ($(window).scrollTop() > headerScrollPos) {
              stricky.addClass('stricky-fixed');
            } else if ($(this).scrollTop() <= headerScrollPos) {
              stricky.removeClass('stricky-fixed');
            }
          }
          OnePageMenuScroll();

        });

      }
    }
</script>

<style scoped>

</style>
