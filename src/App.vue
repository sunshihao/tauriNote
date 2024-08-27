<template>
  <div id="iframe-container">
    <iframe id="my-iframe" :src="src" v-bind="options"></iframe>
  </div>
</template>

<script setup lang="ts">

import { ref, reactive } from "vue";

const src = ref("https://note.dhc.ink");

const options = reactive({
  width: "100%",
  height: "100%",
  frameborder: "0",
  scrolling: "no",
});
</script>

<style scoped>
#iframe-container {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 9999;
}

#iframe-container.fullscreen #my-iframe {
  width: 100%;
  height: 100%;
  border: none;
}
</style>

<style>
html {
  box-sizing: border-box;
}
*,
*:before,
*:after {
  box-sizing: inherit;
}
body,
h1,
h2,
h3,
h4,
p,
figure,
blockquote,
dl,
dd {
  margin: 0;
}

ul[class],
ol[class] {
  margin: 0;
  padding: 0;
  list-style: none;
}
a:not([class]) {
  text-decoration-skip-ink: auto;
  color: currentColor;
}
input,
button,
textarea,
select {
  font: inherit;
}
p,
h1,
h2,
h3,
h4,
h5,
h6 {
  overflow-wrap: break-word;
}

html {
  -moz-text-size-adjust: none;
  -webkit-text-size-adjust: none;
  text-size-adjust: none;
}
</style>
