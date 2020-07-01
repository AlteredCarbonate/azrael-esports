<template>
  <div id="home">
    <div id="section" class="first">
      Lorem ipsum, dolor sit amet consectetur adipisicing elit. Necessitatibus
      architecto error sit, dolorum aliquid sed, quas, modi harum in nemo atque
      ipsam consequuntur magni minima? Ipsam veniam esse ipsa suscipit.
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
</style>

<script>
export default {
  name: "Home",
  data() {
    return {
      page: 0,
      windowTop: 0
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

              console.log("Passedby One");
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

              console.log("Passedby Two");
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

              console.log("Passedby Three");
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

              console.log("Passedby Four");
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
