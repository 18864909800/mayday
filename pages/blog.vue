<template>
  <div>
    <Header />
    <PageHeader title="新闻头条" />
    <Blog />
    <Footer />
  </div>
</template>
<script>
  import Header from "~/components/Header.vue";
  import PageHeader from "~/components/PageHeader.vue";
  import Blog from "~/components/Blog.vue";
  import Footer from "~/components/Footer.vue";
  export default {
    components: {
      Header,
      PageHeader,
      Blog,
      Footer,
    },
    head(){
      return {
        title: "Mayday | 新闻"
      }
    }
  }
</script>
