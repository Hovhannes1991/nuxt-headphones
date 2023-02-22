<template>
    <div class="container">
        <div class="latest_products">
            <h2>Our Latest Products</h2>

            <div class="list">
                <LastProductItem v-for="product in last_products" :product="product" />
            </div>
        </div>
    </div>
</template>

<script setup lang="ts">
const last_products = ref([
    { src: 'headphone-pink.svg', reyting: 4.5, name: 'Pink Headphone', price: 256, color: 'pink' },
    { src: 'headphone-blue.svg', reyting: 4.2, name: 'Pink Headphone', price: 235, color: 'blue' },
    { src: 'headphone-green.svg', reyting: 5, name: 'Pink Headphone', price: 320, color: 'green' },
])
</script>

<style lang="scss" scoped>
.latest_products {
    margin-top: 150px;
}

h2 {
    text-align: center;
}

.list {
    margin-top: 130px;
    display: flex;
    justify-content: center;
    gap: 180px 80px;
    flex-wrap: wrap;
}
</style>