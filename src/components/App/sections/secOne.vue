<template>
  <div class="flex mx-5" style="height: 25%;">
    <Mobile class="inline lg:hidden" />
    <Default class="hidden lg:flex" />
  </div>
</template>

<script>
import secOneDefault from "@/components/App/sections/secOne/secOneDefault.vue";
import secOneMobile from "@/components/App/sections/secOne/secOneMobile.vue";

export default {
  name: "secOne",
  components: {
    Default: secOneDefault,
    Mobile: secOneMobile
  }
};
</script>
