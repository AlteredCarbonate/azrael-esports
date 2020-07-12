<template>
  <div id="header" style="background-color: rgba(0, 0, 0, .55);">
    <div class="w-3/3 md:w-2/3 pl-3 text-left uppercase font-semibold pt-1">
      AZRAEL ESPORTS
    </div>
    <div class="md:hidden border border-r ml-1 sm:ml-4 md:ml-0 mr-2" />
    <button id="default" class="flex-1" style="background-color: transparent;">
      Media
    </button>

    <button id="default" class="flex-1" style="background-color: transparent;">
      Shop
    </button>

    <button id="default" class="flex-1" style="background-color: transparent;">
      Sponsors
    </button>

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

  z-index: 2;
}
</style>
