<template>
  <div>
    <div
      id="title"
      class="text-2xl p-2 text-white border-b border-gray-600"
      style="background-color: var(--darkColor); opacity: 0.65;"
    >
      <p><slot name="title"></slot></p>
    </div>
    <div style="background-color: var(--lightColor); color:white;">
      <div class="bg-white">
        <slot name="img"></slot>
        <!-- <apexglobalseries
          class="w-full p-4"
          color="black"
          detail="#a4adb0"
          style="height: 160px;"
        /> -->
      </div>

      <p class="p-2">
        <slot name="desc">
          Lorem ipsum dolor sit amet consectetur, adipisicing elit. Totam illo
          vel harum iure reiciendis, sequi debitis natus deserunt repellat
          cumque, error similique quae impedit asperiores pariatur possimus
          nihil ea. Necessitatibus.
        </slot>
      </p>
    </div>
    <button id="default" class="w-full">
      MORE
    </button>
  </div>
</template>

<script>
export default {
  name: "imageCanvas",
  props: {
    title: String,
    desc: String,
    img: Object
  }
};
</script>
