<template>
  <div id="home">
    <div id="section" class="first">
      <div class="flex mx-5" style="height: 25%;">

        <div class="imageCanvas">
          <div id="title" class="text-2xl p-2 text-white border-b border-gray-600"
            style="background-color: var(--darkColor); opacity: 0.65;">
            <p>APEX LEGENDS</p>
          </div>
          <div style="background-color: rgba(0,0,0,.25); color: grey;">
            <img style="height: 160px; width: 100%;" src="../assets/logo/apex-globalseries.jpg" alt="apex-globalseries">

            <p class="p-2">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Totam illo vel harum iure
              reiciendis, sequi
              debitis natus deserunt repellat cumque, error similique quae impedit asperiores pariatur possimus nihil
              ea. Necessitatibus.</p>
          </div>
          <button id="default">
            MORE
          </button>
        </div>

        <div class="imageCanvas">
          <img src="../assets/logo/azrael-logoX512.png" alt="azrael-Logo">

          <button id="highlighted" class="w-full mt-6 shadow-inner">
            <p class="text-center text-4xl">
              We want <strong>YOU !</strong>
            </p>
          </button>
        </div>

        <div class="imageCanvas">
          <div id="title" class="text-2xl p-2 text-white border-b border-gray-600"
            style="background-color: var(--darkColor); opacity: 0.65;">
            <p>VALORANT</p>
          </div>
          <div style="background-color: rgba(0,0,0,.25); color: grey;">
            <img class="pt-3" style="height: 160px; width: 100%;" src="../assets/icons/ico_plan.svg"
              alt="apex-globalseries">

            <p class="p-2">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Totam illo vel harum iure
              reiciendis, sequi
              debitis natus deserunt repellat cumque, error similique quae impedit asperiores pariatur possimus nihil
              ea. Necessitatibus.
            </p>
          </div>
          <button id="default">
            MORE
          </button>
        </div>
      </div>
    </div>
    <div id="section" class="second">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempora ab ipsam
      quod sed voluptatem dicta explicabo ipsa animi corporis dignissimos.
      Maiores dolorum recusandae amet culpa rerum mollitia. Dicta, facere
      voluptas?
    </div>
    <div id="section" class="three">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium, quas
      nulla ipsum laudantium quisquam explicabo quod quibusdam optio. Minima
      reprehenderit, aut assumenda dignissimos officia cumque dolorem deleniti
      accusantium expedita? Provident!
    </div>
    <div id="section" class="four">
      Lorem, ipsum dolor sit amet consectetur adipisicing elit. Totam culpa sit
      animi? Sit tempore voluptatem mollitia optio asperiores, aspernatur
      pariatur laboriosam quia quasi magni doloremque, doloribus veritatis non
      suscipit ad?
    </div>
  </div>
</template>

<style scoped>
  #home,
  #section {
    height: 100vh;
    width: 100%;
  }

  #home {
    max-height: 100vh;
    overflow-y: scroll;
    border: 1px solid gray;
    scroll-snap-type: mandatory;
    scroll-snap-points-y: repeat(3rem);
    scroll-snap-type: y mandatory;
  }

  #section {
    scroll-snap-align: start;
  }

  #section:nth-child(0) {
    @apply bg-gray-800;
  }

  #section:nth-child(1) {
    @apply bg-gray-700;
  }

  #section:nth-child(2) {
    @apply bg-gray-600;
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
    background-image: url("../assets/background/tile_darkgraph.png");
    background-size: auto;
    background-position: left;
    background-repeat: repeat;
  }

  #section .imageCanvas {
    @apply w-1/3;
    @apply mx-16;
    padding-top: 15vh;
    height: 100vh;
  }

  #section .imageCanvas:nth-of-type(1) {
    color: black;
  }

  #section .imageCanvas:nth-of-type(2) {}

  #section .imageCanvas:nth-of-type(3) {
    color: black;
  }
</style>

<script>
  export default {
    name: "Home",
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
          function (entries) {
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
          function (entries) {
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
          function (entries) {
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
          function (entries) {
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