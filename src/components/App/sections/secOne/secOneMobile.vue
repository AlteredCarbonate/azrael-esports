<template>
  <div id="section" class="first">
    <div class="imageCanvas w-full" style="height: 350px; padding: 8vh;">
      <img
        class="m-auto"
        src="../../../../assets/logo/azrael-logoX512.png"
        alt="azrael-Logo"
        style="height: 300px;"
      />

      <div class="w-full px-10 lg:px-24">
        <button id="highlighted" class="w-full mt-6">
          <p class="pt-2">WE'RE SEARCHING MEMBERS</p>
          <p class="text-center text-2xl lg:text-4xl">
            We want <strong>YOU !</strong>
          </p>
        </button>
      </div>
    </div>

    <div class="flex" style="padding-top: 3vh;">
      <div class="imageCanvas w-2/3">
        <tplimageCanvas>
          <template #title>
            awdawd
          </template>
          <template #img>
            <apexglobalseries
              class="w-full p-4"
              color="black"
              detail="#a4adb0"
              style="height: 160px;"
          /></template>
          <template #desc>awdawd</template>
        </tplimageCanvas>
      </div>
      <div class="imageCanvas w-1/3"></div>
      <div class="imageCanvas w-2/3">
        <tplimageCanvas>
          <template #title>
            awdawd
          </template>
          <template #img>
            <apexglobalseries
              class="w-full p-4"
              color="black"
              detail="#a4adb0"
              style="height: 160px;"
          /></template>
          <template #desc>awdawd</template>
        </tplimageCanvas>
      </div>
    </div>
  </div>
</template>

<script>
import apexglobalseries from "@/components/Logos/apexglobalseries.vue";
import tplimageCanvas from "@/components/App/sections/secOne/tplimageCanvas.vue";

export default {
  name: "secOneDefault",
  components: {
    apexglobalseries,
    tplimageCanvas
  }
};
</script>

<style></style>
