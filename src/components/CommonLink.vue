<script setup lang="ts">
import type { RouteLocationRaw } from "vue-router";

defineProps<{ to: RouteLocationRaw }>();
</script>

<template>
  <router-link
    :to="to"
    class="text-gray-500 hover:text-gray-950 hover:underline transition-all duration-300"
  >
    <slot />
  </router-link>
</template>
