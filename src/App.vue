<!-- <router-link to="/">Home</router-link> -->
<template>
  <div id="app">
    <tplApp>
      <router-view />
    </tplApp>
  </div>
</template>

<style>
:root {
  /*
      NEW
    */
  --backgroundColor: #adb5bd;
  --darkColor: #212529;
  --lightColor: #495057;
  /*
      OLD
    */
  --primaryColor: #fff;

  --alertColor: #f2dede;
  --alertTextColor: #a94442;

  --borderColor: #eaecef;
  --borderStrength: 1px;
}

html,
body,
#app {
  @apply w-full;
  @apply h-full;

  color: #626262;
  background-color: transparent;
}
</style>
<!--
  Color Palette
  https://coolors.co/f8f9fa-e9ecef-dee2e6-ced4da-adb5bd-6c757d-495057-343a40-212529

  Darken
  https://www.hexcolortool.com/
-->

<script>
import tplApp from "@/templates/views/tplApp.vue";

export default {
  components: {
    tplApp
  },
  data() {
    return {
      title: "Azrael Esports",
      copyright: "Azrael Esports © 2020",
      credits: "Ramon Pawlowski"
    };
  },
  mounted() {
    document.title = this.title;
  }
};
</script>
