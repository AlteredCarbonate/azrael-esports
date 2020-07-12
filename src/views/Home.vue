<template>
  <div id="home">
    <div id="section" class="first">
      <secOne />
      <!-- <secOnePart2Mobile /> -->
    </div>
    <secTwo />
    <secThree />
  </div>
</template>

<style>
#home,
#section {
  height: 100vh;
  width: 100%;
}
@media (min-width: 640px) {
  #home {
    scroll-snap-type: mandatory;
    scroll-snap-points-y: repeat(3rem);
    scroll-snap-type: y mandatory;
  }
}
#home {
  max-height: 100vh;
  overflow-y: scroll;
  border: 1px solid gray;
}

#section {
  scroll-snap-align: start;
}

#section:nth-child(3) {
  @apply bg-gray-500;
}

#section:nth-child(4) {
  @apply bg-gray-400;
}

/*
  First Section
*/
#section.first {
  background-image: url("../assets/background/bg-tile-v6.svg");
  background-size: 65px;
  background-position: left;
  background-repeat: repeat;
  background-color: var(--backgroundColor);
}

#section .imageCanvas {
  @apply w-1/3;
  @apply m-auto;
  padding-top: 15vh;
  height: 100vh;
}

#section .imageCanvas:nth-of-type(1) > div {
  color: black;
}

#section .imageCanvas:nth-of-type(2) {
}

#section .imageCanvas:nth-of-type(3) > div {
  @apply shadow-xl;
  color: black;
}

/*
    Second Section
  */
#section.second {
  @apply p-4;

  background-color: var(--backgroundColor);
  background-image: url("../assets/background/tile_darkgrid.png");
  background-size: 100px;
  background-position: left;
  background-repeat: repeat;
}

/*
  Third Section
*/
#section.third {
  @apply p-4;
  @apply text-white;

  background-color: var(--backgroundColor);
  background-image: url("../assets/background/tile_darkgrid.png");
  background-size: 100px;
  background-position: left;
  background-repeat: repeat;
}
</style>

<script>
import secOne from "@/components/App/sections/secOne.vue";
import secTwo from "@/components/App/sections/secTwo.vue";
import secThree from "@/components/App/sections/secThree.vue";

export default {
  name: "Home",
  components: {
    secOne,
    secTwo,
    secThree
  },
  data() {
    return {
      page: 0
    };
  },
  mounted() {
    this.onScroll();
  },
  methods: {
    onScroll() {
      var observerOne = new IntersectionObserver(
        function(entries) {
          entries.forEach(entry => {
            const { isIntersecting } = entry;
            if (isIntersecting === true) {
              this.page = 1;
              console.log(this.page);
            }
          });
        },
        { threshold: 0.1 }
      );

      var observerTwo = new IntersectionObserver(
        function(entries) {
          entries.forEach(entry => {
            const { isIntersecting } = entry;
            if (isIntersecting === true) {
              this.page = 2;
              console.log(this.page);
            }
          });
        },
        { threshold: 0.1 }
      );

      var observerThree = new IntersectionObserver(
        function(entries) {
          entries.forEach(entry => {
            const { isIntersecting } = entry;
            if (isIntersecting === true) {
              this.page = 3;
              console.log(this.page);
            }
          });
        },
        { threshold: 0.1 }
      );

      var observerFour = new IntersectionObserver(
        function(entries) {
          entries.forEach(entry => {
            const { isIntersecting } = entry;
            if (isIntersecting === true) {
              this.page = 4;
              console.log(this.page);
            }
          });
        },
        { threshold: 0.1 }
      );

      observerOne.observe(document.querySelector(".first"));
      observerTwo.observe(document.querySelector(".second"));
      observerThree.observe(document.querySelector(".three"));
      observerFour.observe(document.querySelector(".four"));
    }
  }
};
</script>
