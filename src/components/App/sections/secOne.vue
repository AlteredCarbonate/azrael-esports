<template>
  <div id="section" class="first">
    <div class="flex mx-5" style="height: 25%;">
      <Mobile class="inline lg:hidden" />
      <Default class="hidden lg:flex overflow-y-auto" />
    </div>
  </div>
</template>

<script>
import secOneDefault from "@/components/App/sections/secOne/components/secOneDefault.vue";
import secOneMobile from "@/components/App/sections/secOne/components/secOneMobile.vue";

export default {
  name: "secOne",
  components: {
    Default: secOneDefault,
    Mobile: secOneMobile
  }
};
</script>
