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
    --lightColor: #535558;
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

  .unselectable {
    -webkit-touch-callout: none;
    -webkit-user-select: none;
    -khtml-user-select: none;
    -moz-user-select: none;
    -ms-user-select: none;
    user-select: none;
  }

  /*
  Button
*/

  button:active,
  button:focus,
  button {
    outline: 0px !important;
  }

  button#highlighted,
  button#default {
    @apply text-center;
    @apply py-1;
    @apply px-2;
    @apply rounded-sm;
    @apply text-white;
    transition: background-color 0.2s linear;
  }

  button#default {
    @apply w-full;
    @apply border-b;
    border-color: transparent;

    background-color: rgba(0, 0, 0, .65);
    transition: border 0.2s linear;

  }

  button#highlighted {
    animation-name: highlight;
    animation-duration: 3s;
    animation-delay: 1s;
    animation-iteration-count: infinite;
    animation-timing-function: linear;

    transition: border-width 0.2s linear;
  }

  button#default:hover {
    @apply border-white;
  }

  button#default:active {
    @apply border-gray-500;
  }

  button#default+button#default {
    @apply mx-1;
  }

  .imageCanvas {
    clip-path: url("./assets/shapes/imageCanvas.svg#path");
  }

  /*
    Animations
  */
  @keyframes highlight {
    0% {
      border-width: 1px;
      border-color: transparent;
    }

    50% {
      border-color: white;
    }

    100% {
      border-width: 1px;
      border-color: transparent;
    }
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