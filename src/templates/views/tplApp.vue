<template>
  <div>
    <Header />
    <slot />
  </div>
</template>

<script>
import Header from "@/components/App/Header.vue";

export default {
  components: {
    Header
  }
};
</script>
