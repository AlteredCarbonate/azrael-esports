<template>
  <div id="section" class="first">
    <div class="imageCanvas w-full" style="height: 350px; padding: 12vh;">
      <img
        class="m-auto"
        src="../../../../../assets/logo/azrael-logoX512.png"
        alt="azrael-Logo"
        style="width: 50vh;"
        v-tilt="{ reverse: true, perspective: 1200, speed: 500 }"
      />

      <div class="px-10 lg:px-24">
        <button id="highlighted" class="w-full mt-6">
          <p class="text-center text-2xl lg:text-4xl">
            We want <strong>YOU !</strong>
          </p>
          <p class="pt-2">WE'RE SEARCHING MEMBERS</p>
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "secOneDefault"
};
</script>

<style></style>
