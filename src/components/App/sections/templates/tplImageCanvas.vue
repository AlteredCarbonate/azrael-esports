<template>
  <div class="shadow-xl" style="border: 1px solid rgba(40,40,40,.5);">
    <div
      id="title"
      class="text-2xl p-2 text-white border-b border-gray-600"
      style="background-color: var(--darkColor); opacity: 0.65;"
    >
      <p><slot name="title" /></p>
    </div>
    <div style="background-color: var(--lightColor); color:white;">
      <div class="bg-white">
        <slot name="img" />
      </div>

      <p class="p-2">
        <slot name="desc" />
      </p>
    </div>
    <button id="default" class="w-full">
      MORE
    </button>
  </div>
</template>

<script>
export default {
  name: "tplImageCanvas",
  props: {
    title: String,
    desc: String,
    img: Object
  }
};
</script>
