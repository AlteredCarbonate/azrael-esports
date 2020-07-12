<template>
  <tplImageCanvas>
    <template #title>
      VALORANT
    </template>
    <template #img>
      <img
        class="py-3 bg-white"
        style="height: 160px; width: 100%;"
        src="../../../../assets/icons/ico_plan.svg"
        alt="apex-globalseries"
      />
    </template>
    <template #desc>
      <strong>VALORANT</strong> a 5v5 character-based tactical FPS where precise
      gunplay meets unique agent abilities <br /><br />
      BLA BLA BLA
    </template>
  </tplImageCanvas>
</template>

<script>
import tplImageCanvas from "../templates/tplImageCanvas.vue";

export default {
  name: "valorantImageCanvas",
  components: {
    tplImageCanvas
  }
};
</script>
