<template>
  <div class="flex mx-5" style="height: 25%;">
    <Default />
  </div>
</template>

<script>
import secOneDefault from "@/components/App/sections/secOne/secOneDefault.vue";
export default {
  name: "secOne",
  components: {
    Default: secOneDefault
  }
};
</script>
