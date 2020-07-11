<template>
  <div id="header" class="" style="background-color: rgba(0, 0, 0, .55);">
    <div class="w-2/3 pl-2 text-left uppercase font-semibold pt-1">
      AZRAEL ESPORTS
    </div>
    <button id="default" class="flex-1" style="background-color: transparent;">
      Media
    </button>
    <div class="border border-r mr-2 ml-1" />

    <button id="default" class="flex-1" style="background-color: transparent;">
      Shop
    </button>
    <div class="border border-r mr-2 ml-1" />
    <button id="default" class="flex-1" style="background-color: transparent;">
      Sponsors
    </button>
    <div class="border border-r mr-2 ml-1" />

    <button id="default" class="flex-1" style="background-color: transparent;">
      Partnerships
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
  @apply flex;
  @apply top-0;
  @apply pr-5;
  @apply py-1;
  @apply text-white;

  @apply border-b;
  border-color: rgba(25, 25, 25, 0.25);
}
</style>
