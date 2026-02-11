<script setup lang="ts">
import type { NuxtError } from "#app";

defineProps<{
  error: NuxtError;
}>();

const goHome = () => {
  navigateTo("/");
};
</script>

<template>
  <div class="error__wrapper">
    <h1 class="error__status">{{ error.status }}</h1>
    <div
      v-if="error.status === 404"
      class="error__message"
    >
      Страница не найдена, вернитесь на главную страницу
    </div>
    <div
      v-else
      class="error__message"
    >
      {{ error.message }}
    </div>
    <ActionButton
      class="error__button"
      @click="goHome"
    >
      На главную
    </ActionButton>
  </div>
</template>

<style scoped>
.error__wrapper {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
}

.error__status {
  font-weight: 500;
  font-size: 120px;
  margin: 0;
  color: var(--color-black-light);
}

.error__message {
  font-weight: 300;
  font-size: 16px;
  line-height: 150%;
  text-align: center;
  color: var(--color-black-light);
  margin-bottom: 24px;
}

.error__button {
  width: 300px;
}
</style>
