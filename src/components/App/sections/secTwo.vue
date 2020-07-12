<template>
  <div id="section" class="second text-center flex">
    <div id="apex" class="w-2/6 my-10">
      <apexglobalseries
        class="pt-5 sm:pt-10 lg:pt-16 md:pt-12 px-4 w-full h-48 lg:h-56 xl:h-64"
        color="white"
        detail="#a4adb0"
        stroke="black"
      />
    </div>
    <div class="w-4/6 px-4 pt-10 mt-10 text-left text-white">
      <div id="team" class="p-4">
        <p class="text-3xl font-medium">
          Our Team
        </p>
        <div class="flex pt-2">
          <div id="members" class="flex">
            <div
              id="memberModal"
              v-for="member in members.apex.user"
              :key="member.name"
            >
              <Member
                :Member="member.name"
                :Desc="member.desc"
                :Media="member.media"
              ></Member>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import apexglobalseries from "@/components/Logos/apexglobalseries.vue";
import Member from "@/components/App/sections/secTwo/components/Member.vue";

export default {
  name: "secTwo",
  data() {
    return {
      members: {
        apex: {
          count: 0,
          user: [
            {
              id: 0,
              name: "gloomy",
              desc: "The Friendly Boy",
              media: [
                {
                  id: 0,
                  name: "instagram",
                  link: "https://instagram.com"
                },
                {
                  id: 1,
                  name: "youtube",
                  link: "https://youtube.com"
                }
              ]
            },
            {
              id: 1,
              name: "gloomy",
              desc: "The Friendly Boy",
              media: [
                {
                  id: 0,
                  name: "instagram",
                  link: "https://instagram.com"
                },
                {
                  id: 1,
                  name: "youtube",
                  link: "https://youtube.com"
                }
              ]
            }
          ]
        },
        valorant: {}
      }
    };
  },
  components: {
    apexglobalseries,
    Member
  }
};
</script>

<style scoped>
#section #apex {
  background-image: url("../../../assets/background/red_background3.png");
  background-size: contain;
  background-repeat: no-repeat;
  background-position: top;
}

#members {
  @apply p-4;
  @apply text-center;
  @apply select-none;
}

#memberModal + #memberModal {
  @apply mx-10;
}

#member-media {
  @apply p-2;
}

#media {
  @apply select-none;
}
</style>
