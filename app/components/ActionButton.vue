<script setup lang="ts"></script>

<template>
  <button class="action-button">
    <slot />
  </button>
</template>

<style scoped>
.action-button {
  border-radius: 20px;
  cursor: pointer;
  background-color: var(--color-black);
  padding: 10px;

  font-weight: 500;
  font-size: 16px;
  text-align: center;
  color: var(--color-white);
}
</style>
