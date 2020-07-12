<template>
  <tplImageCanvas>
    <template #title>
      APEX LEGENDS
    </template>
    <template #img>
      <apexglobalseries
        class="w-full p-4"
        color="black"
        detail="#a4adb0"
        style="height: 160px;"
    /></template>
    <template #desc>
      <strong>APEX LEGENDS </strong>a free-to-play Battle Royale game where
      legendary competitors battle for glory, fame, and fortune on the fringes
      of the Frontier. <br /><br />
      BLA BLA BLA
    </template>
  </tplImageCanvas>
</template>

<script>
import apexglobalseries from "@/components/Logos/apexglobalseries.vue";
import tplImageCanvas from "../templates/tplImageCanvas.vue";

export default {
  name: "apexImageCanvas",
  components: {
    apexglobalseries,
    tplImageCanvas
  }
};
</script>
