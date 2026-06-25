<script setup lang="ts">
import { FloatingLines } from "@/components/ui/floating-lines";
</script>

<template>
  <!-- Project-wide animated background: rendered once, persists across routes,
       sits behind all content, and is click-through so it never blocks the UI.
       bg-black is required because the component uses mix-blend-mode: screen. -->
  <div class="fixed inset-0 -z-10 bg-black">
    <FloatingLines
      class="pointer-events-none"
      :lines-gradient="['#1f2937', '#4b5563', '#9ca3af']"
      :animation-speed="0.5"
      :interactive="false"
    />
  </div>

  <RouterView />
</template>
