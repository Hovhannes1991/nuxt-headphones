<template>
  <div class="complectation_info">
    <img class="bug_image" src="images/boxing.png" alt="image" />

    <div class="items_list">
      <h2 class="title section_title">
        Whatever you get<br />
        in the box
      </h2>

      <div class="items">
        <div class="item" v-for="item in complectation_items" :key="item">
          <img src="icons/arrow-right.svg" alt="arrow icon" />
          <span>{{ item }}</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
const complectation_items = ref([
  "5A charger",
  "Extra batery",
  "Sophisticated bag",
  "User manual guide",
]);
</script>

<style lang="scss" scoped>
.complectation_info {
  display: flex;
  justify-content: space-between;
  gap: 50px;
  padding: 0 150px;
  @media only screen and (max-width: 1500px) {
    gap: 20px;
    padding: 0 70px;
  }
  @media only screen and (max-width: 1250px) {
    flex-direction: column;
    align-items: center;
    gap: 100px;
  }

  img.bug_image {
    max-width: 450px;
    @media only screen and (max-width: 1700px) {
      max-width: 350px;
    }
  }

  .items_list {
    .title {
      color: #000;
      margin-bottom: 50px;
    }

    .items {
      .item {
        height: 50px;
        display: flex;
        align-items: center;
        gap: 10px;
        border-bottom: 1px solid #cecece;
        font-size: 22px;
      }
    }
  }
}
</style>
