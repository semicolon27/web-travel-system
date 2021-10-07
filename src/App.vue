<template>
  <!-- <metainfo>
    <template v-slot:title="{ content }">
      {{ content ? `${content} | ${siteName}` : siteName }}
    </template>
  </metainfo>
  <router-view /> -->
  <c-navbar></c-navbar>
  <div class="rounded-lg shadow bg-base-200 drawer drawer-mobile container">
    <input id="my-drawer-2" type="checkbox" class="drawer-toggle" />
    <div class="flex flex-col items-center justify-center drawer-content">
      <metainfo>
        <template v-slot:title="{ content }">
          {{ content ? `${content} | ${siteName}` : siteName }}
        </template>
      </metainfo>
      <router-view />
    </div>
    <c-drawer></c-drawer>
  </div>
</template>

<script setup lang="ts">
import { useMeta } from "vue-meta";

const siteName = "Web Travel System";

useMeta({
  title: "",
  htmlAttrs: { lang: "en", amp: true },
});
</script>
