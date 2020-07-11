<template>
  <div class="flex mx-5" style="height: 25%;">
    <div class="imageCanvas w-2/3 lg:w-1/5">
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

    <div class="imageCanvas w-1/3 lg:w-2/5">
      <img
        class="m-auto"
        src="../../../assets/logo/azrael-logoX512.png"
        alt="azrael-Logo"
      />

      <div class="w-full px-10 lg:px-24">
        <button id="highlighted" class="w-full mt-6 shadow-inner">
          <p class="text-center text-2xl lg:text-4xl">
            We want <strong>YOU !</strong>
          </p>
        </button>
      </div>
    </div>

    <div class="imageCanvas w-2/3 lg:w-1/5">
      <div
        id="title"
        class="text-2xl p-2 text-white border-b border-gray-600"
        style="background-color: var(--darkColor); opacity: 0.65;"
      >
        <p>VALORANT</p>
      </div>
      <div style="background-color: var(--lightColor); color: white;">
        <div>
          <img
            class="py-3"
            style="height: 160px; width: 100%; background-color: rgba(175, 175, 175, 0.986);"
            src="../../../assets/icons/ico_plan.svg"
            alt="apex-globalseries"
          />
        </div>
        <p class="p-2">
          Lorem ipsum dolor sit amet consectetur, adipisicing elit. Totam illo
          vel harum iure reiciendis, sequi debitis natus deserunt repellat
          cumque, error similique quae impedit asperiores pariatur possimus
          nihil ea. Necessitatibus.
        </p>
      </div>
      <button id="default" class="w-full">MORE</button>
    </div>
  </div>
</template>

<script>
import apexglobalseries from "@/components/Logos/apexglobalseries.vue";
import tplimageCanvas from "@/components/App/sections/secOne/tplimageCanvas.vue";
export default {
  name: "secOne",
  components: {
    apexglobalseries,
    tplimageCanvas
  }
};
</script>
