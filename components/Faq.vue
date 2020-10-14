<template>
  <section class="faq-one">
    <img src="/assets/images/background/faq-one-bg.png" alt="Awesome Image" class="faq-one__bg" />
    <div class="container">
      <div class="block-title text-center">
        <h2 class="block-title__title">Want to Ask <span>Something</span> <br> From Us?</h2><!-- /.block-title__title -->
      </div><!-- /.block-title -->
      <div class="accrodion-grp" data-grp-name="faq-accrodion">
        <div class="accrodion active wow fadeInUp" data-wow-duration="1500ms" data-wow-delay="0ms">
          <div class="accrodion-inner">
            <div class="accrodion-title">
              <h4>Pre and post launch mobile app marketing pitfalls to avoid</h4>
            </div>
            <div class="accrodion-content">
              <div class="inner">
                <p>There are many variations of passages of available but majority have alteration in some by inject humour or random words. Lorem ipsum dolor sit amet, error insolens reprimique no quo, ea pri verterem phaedr vel ea iisque aliquam.</p>
              </div><!-- /.inner -->
            </div>
          </div><!-- /.accrodion-inner -->
        </div>
        <div class="accrodion  wow fadeInUp" data-wow-duration="1500ms" data-wow-delay="100ms">
          <div class="accrodion-inner">
            <div class="accrodion-title">
              <h4>Boostup your application traffic is just a step away</h4>
            </div>
            <div class="accrodion-content">
              <div class="inner">
                <p>There are many variations of passages of available but majority have alteration in some by inject humour or random words. Lorem ipsum dolor sit amet, error insolens reprimique no quo, ea pri verterem phaedr vel ea iisque aliquam.</p>
              </div><!-- /.inner -->
            </div>
          </div><!-- /.accrodion-inner -->
        </div>
        <div class="accrodion wow fadeInUp" data-wow-duration="1500ms" data-wow-delay="200ms">
          <div class="accrodion-inner">
            <div class="accrodion-title">
              <h4>How to update application new features</h4>
            </div>
            <div class="accrodion-content">
              <div class="inner">
                <p>There are many variations of passages of available but majority have alteration in some by inject humour or random words. Lorem ipsum dolor sit amet, error insolens reprimique no quo, ea pri verterem phaedr vel ea iisque aliquam.</p>
              </div><!-- /.inner -->
            </div>
          </div><!-- /.accrodion-inner -->
        </div>
        <div class="accrodion wow fadeInUp" data-wow-duration="1500ms" data-wow-delay="300ms">
          <div class="accrodion-inner">
            <div class="accrodion-title">
              <h4>How to connect with the support to improve app experience</h4>
            </div>
            <div class="accrodion-content">
              <div class="inner">
                <p>There are many variations of passages of available but majority have alteration in some by inject humour or random words. Lorem ipsum dolor sit amet, error insolens reprimique no quo, ea pri verterem phaedr vel ea iisque aliquam.</p>
              </div><!-- /.inner -->
            </div>
          </div><!-- /.accrodion-inner -->
        </div>
      </div>
    </div><!-- /.container -->
  </section>
</template>

<script>
    export default {
      name: "Faq",
      mounted() {
        if ($('.accrodion-grp').length) {
          var accrodionGrp = $('.accrodion-grp');
          accrodionGrp.each(function() {
            var accrodionName = $(this).data('grp-name');
            var Self = $(this);
            var accordion = Self.find('.accrodion');
            Self.addClass(accrodionName);
            Self.find('.accrodion .accrodion-content').hide();
            Self.find('.accrodion.active').find('.accrodion-content').show();
            accordion.each(function() {
              $(this).find('.accrodion-title').on('click', function() {
                if ($(this).parent().parent().hasClass('active') === false) {
                  $('.accrodion-grp.' + accrodionName).find('.accrodion').removeClass('active');
                  $('.accrodion-grp.' + accrodionName).find('.accrodion').find('.accrodion-content').slideUp();
                  $(this).parent().parent().addClass('active');
                  $(this).parent().parent().find('.accrodion-content').slideDown();
                };


              });
            });
          });

        }
      }
    }
</script>

<style scoped>

</style>
