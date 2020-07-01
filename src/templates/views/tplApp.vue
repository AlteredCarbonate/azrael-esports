<template>
  <div>
    <Header />
    <slot />
    <Footer />
  </div>
</template>

<script>
import Header from "@/components/App/Header.vue";
import Footer from "@/components/App/Footer.vue";

export default {
  components: {
    Header,
    Footer
  }
};
</script>

<style></style>
