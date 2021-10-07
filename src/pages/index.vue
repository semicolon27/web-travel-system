<template>
  <div>
    <c-button> Save </c-button>
    <button class="btn btn-wide btn-lg">large</button>
  </div>
</template>

<script setup>
import { useMeta } from "vue-meta";
import { computed, ref, onMounted } from "vue";
import { useRouter } from "vue-router";

onMounted(() => {
  console.log("helo");
});

useMeta({
  title: "Homepage",
});
</script>
