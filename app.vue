<template>
  <div class="app">
    <div class="container">
      <TheHeader />
      <LatestCollection />
      <HeadphoneInfo />
      <LatestProducts />
      <ComplectationInfo />
      <SubscribeSection />
      <TheFooter />
    </div>
  </div>
</template>

<script setup lang="ts">
</script>

<style>
.app {
  max-width: 1920px;
  height: 100vh;
  display: flex;
  margin: 0 auto;
}

.container {
  width: 70%;
  display: flex;
  flex-direction: column;
  gap: 130px;
  margin: 0 auto;
}
</style>
