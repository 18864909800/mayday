<template>
  <div>
    <Header />
    <PageHeader title="新闻详情" />
    <BlogDetails />
    <Footer />
  </div>
</template>
<script>
  import Header from "~/components/Header.vue";
  import PageHeader from "~/components/PageHeader.vue";
  import BlogDetails from "~/components/BlogDetails.vue";
  import Footer from "~/components/Footer.vue";
  export default {
    components: {
      Header,
      PageHeader,
      BlogDetails,
      Footer
    },
    head(){
      return {
        title: "Mayday | 新闻 Details"
      }
    }
  }
</script>
