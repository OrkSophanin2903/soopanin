<script setup lang="ts">
import { useSlots } from "vue";
import { cn } from "@/lib/utils";
import { GlassSurface } from "@/components/ui/glass-surface";

const props = withDefaults(
  defineProps<{
    class?: string;
    borderRadius?: number;
  }>(),
  {
    borderRadius: 24,
  },
);

const slots = useSlots();
</script>

<template>
  <!-- width/height as strings override GlassSurface's 200x80 pill defaults so the
       card fills its container and grows with its content. Any other glass knob
       (blur, brightness, distortionScale, ...) falls through to GlassSurface. -->
  <GlassSurface
    width="100%"
    height="auto"
    :border-radius="borderRadius"
    :class="cn('w-full', props.class)"
  >
    <!-- w-full overrides .gs-content's centering; flex-col + text-left lays the
         regions out like a card. Light text because it floats over the dark bg. -->
    <div class="flex w-full flex-col gap-4 p-4 text-left text-white sm:p-6">
      <div v-if="slots.header" class="flex flex-col gap-1.5">
        <slot name="header" />
      </div>

      <div v-if="slots.default" class="text-sm text-white/90">
        <slot />
      </div>

      <div v-if="slots.footer" class="flex flex-wrap items-center gap-2 pt-2">
        <slot name="footer" />
      </div>
    </div>
  </GlassSurface>
</template>
