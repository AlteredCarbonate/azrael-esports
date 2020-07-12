<template>
  <div id="memberCanvas">
    <img
      class="rounded-full"
      draggable="false"
      :src="require('../../../../../assets/members/apex/' + Member + '.png')"
      alt="member-avatar"
    />
    <p class="pt-2 text-lg font-medium uppercase">
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
  },
  mounted() {
    var median = this.Media;
    for (var i in median) {
      console.log(median[i].name);
      console.log(median[i].link);
    }
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

#media img {
  @apply h-10;
}
img {
  @apply m-auto;
  @apply p-2;
}
</style>
