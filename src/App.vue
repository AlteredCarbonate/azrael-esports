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
  --backgroundColor: #5d5c5c;
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
  @apply select-none;
  @apply w-full;
  @apply h-full;

  color: #626262;
  background-color: transparent;
}

/*
  Scrollbar
*/
::-webkit-scrollbar {
  width: 0.5rem;
}

::-webkit-scrollbar-track {
  background: #dfe6e9;
}

::-webkit-scrollbar-thumb {
  background: #b2bec3;
}

::-webkit-scrollbar-thumb:hover {
  background: #7d868a;
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
  @apply border-b;
  border-color: transparent;

  background-color: var(--darkColor);
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

button#default + button#default {
  @apply mx-1;
}

/*
    Animations
  */

div#apex {
  transition: all 0.2s linear;
}

@keyframes highlight {
  0% {
    box-shadow: none;
    border-width: 1px;
    border-color: transparent;
  }

  50% {
    box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1),
      0 10px 10px -5px rgba(0, 0, 0, 0.04);
    border-color: white;
  }

  100% {
    box-shadow: none;
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
      copyright: "Azrael Esports © 2020",
      credits: "Ramon Pawlowski"
    };
  }
};
</script>
