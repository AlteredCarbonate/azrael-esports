<template>
  <div id="memberCanvas" class="w-40 lg:w-48">
    <img
      class="rounded-full h-20"
      draggable="false"
      :src="require('../../../../../assets/members/apex/' + Member + '.png')"
      alt="member-avatar"
      v-tilt="{ reverse: true, perspective: 1500 }"
    />
    <p class="pt-2 text-base lg:text-lg font-medium uppercase">
      {{ Member }}
    </p>
    <p class="font-thin">
      {{ Desc }}
    </p>
    <div id="member-media" class="inline-flex w-full pt-2">
      <div v-for="media in Media" :key="media.id" class="m-auto">
        <a :href="media.link">
          <div id="media">
            <img
              draggable="false"
              :src="
                require('../../../../../assets/members/media/' +
                  media.name +
                  '.png')
              "
              :alt="media.name"
            />
          </div>
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Member",
  props: {
    Member: String,
    Desc: String,
    Media: Array
  }
};
</script>

<style scoped>
#memberCanvas {
  @apply p-2;
  @apply rounded-lg;
  background-color: rgba(0, 0, 0, 0.4);
  border: 1px solid rgba(25, 25, 25, 0.4);
}
#member-media > a {
  @apply m-auto;
}

img {
  @apply m-auto;
  @apply p-2;
}
/*
  MEDIA
 */
#media img {
  @apply h-10;
}

#media {
  transition: background-color 0.2s linear;
}

#media:hover {
  background-color: rgba(25, 25, 25, 0.4);
}
#media:active {
  background-color: rgba(25, 25, 25, 1);
}
</style>
