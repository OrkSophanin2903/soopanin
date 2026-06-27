<script setup lang="ts"></script>

<template>
  <main class="grid min-h-screen place-items-center">
    <RouterView v-slot="{ Component }">
      <Transition name="page" mode="out-in">
        <component :is="Component" />
      </Transition>
    </RouterView>
  </main>
</template>

<style scoped>
.page-enter-active,
.page-leave-active {
  transition: opacity 300ms ease;
}

.page-enter-from,
.page-leave-to {
  opacity: 0;
}
</style>
