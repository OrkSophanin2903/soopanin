<script setup lang="ts">
defineProps<{ href: string; label: string; color?: string }>();
</script>

<template>
  <a
    :href="href"
    :aria-label="label"
    target="_blank"
    rel="noopener noreferrer"
    :style="{ '--brand-color': color }"
    class="[&_svg]:size-5 text-gray-500 hover:text-(--brand-color) transition-colors duration-300"
  >
    <slot />
  </a>
</template>
