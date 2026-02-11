<script setup lang="ts"></script>

<template>
  <div class="menu-container">
    <div class="menu">
      <NuxtLink
        to="/"
        class="home"
      >
        <Icon name="icons:home" />
      </NuxtLink>
      <NuxtLink
        to="/logout"
        class="logout"
      >
        <Icon name="icons:logout" />
      </NuxtLink>
    </div>
  </div>
</template>

<style lang="css" scoped>
.menu-container {
  width: 80px;
}
.menu {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
  width: 80px;
  height: 100vh;
  position: fixed;
  border: 1px solid var(--color-gray);
}
.home {
  margin-top: 42px;
}
.logout {
  margin-bottom: 21px;
}
</style>
