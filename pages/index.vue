<template>
  <div>
    <Header />
    <Banner />
    <Video />
    <Testimonial />
    <Brands />
    <Screenshots />
    <Footer />
  </div>
</template>
<script>
  import Header from "~/components/Header.vue";
  import Banner from "~/components/Banner.vue";
  import Video from "~/components/Video.vue";
  import Testimonial from "~/components/Testimonial.vue";
  import Brands from "~/components/Brands.vue";
  import Counter from "~/components/Counter.vue";
  import Screenshots from "~/components/Screenshots.vue";
  import Footer from "~/components/Footer.vue";
  export default {
    components: {
      Header,
      Banner,
      Video,
      Testimonial,
      Brands,
      Counter,
      Screenshots,
      Footer,
    }
  }
</script>
