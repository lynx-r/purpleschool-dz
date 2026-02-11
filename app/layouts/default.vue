<script setup lang="ts"></script>

<template>
  <div class="layout">
    <LayoutMenu />
    <main>
      <slot />
    </main>
  </div>
</template>

<style lang="css" scoped>
.layout {
  display: flex;
}

.layout main {
  margin-left: 136px;
  width: 100%;
  max-width: 692px;
}
</style>
