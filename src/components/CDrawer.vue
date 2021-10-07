<template>
  <div class="drawer-side">
    <label for="my-drawer" class="drawer-overlay"></label>
    <ul class="menu p-4 overflow-y-auto w-80 bg-base-100 text-base-content">
      <li v-for="nav1 in navigationList">
        <router-link  class="hidden-sibling">{{ nav1.title }}</router-link >
      </li>
    </ul>
  </div>
</template>

<script lang="ts">
import json from "../data/navigation.json";
export default {
  data() {
    return {
      navigationList: [],
    };
  },
  async mounted() {
    this.navigationList = json;
    console.log(this.navigationList);
  },
};
</script>
