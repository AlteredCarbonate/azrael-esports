<template>
  <div id="header" class="flex pt-1">
    <div class="w-2/3"></div>
    <button id="default" class="flex-1" style="background-color: transparent;">
      Twitch
    </button>
    <button id="default" class="flex-1" style="background-color: transparent;">
      Sponsors
    </button>
    <button id="default" class="flex-1" style="background-color: transparent;">
      News Feed
    </button>
  </div>
</template>

<script>
export default {
  name: "Header"
};
</script>

<style scoped>
#header {
  @apply w-full;
  @apply absolute;
  @apply top-0;
  @apply pr-5;
}
</style>
