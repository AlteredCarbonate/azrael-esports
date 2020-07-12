<template>
  <div id="section" class="first flex">
    <div class="imageCanvas w-2/3 lg:w-1/5">
      <apexImageCanvas></apexImageCanvas>
    </div>

    <div class="imageCanvas w-1/3 lg:w-2/5">
      <img
        class="m-auto"
        src="../../../../../assets/logo/azrael-logoX512.png"
        alt="azrael-Logo"
        style="height: 55vh;"
      />

      <div class="w-full px-10 lg:px-24">
        <button id="highlighted" class="w-full mt-6 shadow-inner">
          <p class="text-center text-2xl lg:text-4xl">
            We want <strong>YOU !</strong>
          </p>
          <p class="pt-2">WE'RE SEARCHING MEMBERS</p>
        </button>
      </div>
    </div>

    <div class="imageCanvas w-2/3 lg:w-1/5">
      <valorantImageCanvas></valorantImageCanvas>
    </div>
  </div>
</template>

<script>
import apexImageCanvas from "@/components/App/sections/imageCanvas/apexImageCanvas.vue";
import valorantImageCanvas from "@/components/App/sections/imageCanvas/valorantImageCanvas.vue";

export default {
  name: "secOneDefault",
  components: {
    apexImageCanvas,
    valorantImageCanvas
  }
};
</script>

<style></style>
