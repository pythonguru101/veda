<template>
  <div id="app">
    <router-view></router-view>
  </div>
</template>

<script>
import { provide } from "vue";
import store from "./store";
export default {
  name: "App",
  setup() {
    provide("store", store);
  },
};
</script>

<style>
@import "./styles/index.css";
</style>
