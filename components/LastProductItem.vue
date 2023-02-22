<template>
    <div class="last_product_item">
        <div class="image_wrapper">
            <div class="cart_icon_wrapper cursor-pointer flex-center">
                <div class="bachgraund_shape" :style="{ backgroundColor: props.product.color }"></div>
                <img src="icons/cart.svg" alt="cart">
            </div>

            <div class="bachgraund_shape" :style="{ backgroundColor: props.product.color }"></div>

            <img :src="'images/' + product.src" alt="headphone">
        </div>

        <div class="reyting">
            <ReytingValue :reyting="props.product.reyting" />

            <span class="reyting_text">{{ props.product.reyting }}</span>
        </div>

        <div class="name_and_price">
            <div class="name">{{ props.product.name }}</div>
            <div class="price">$ {{ props.product.price }}</div>
        </div>
    </div>
</template>

<script setup lang="ts">
interface ILastProduvtItemProps {
    src: string;
    reyting: number;
    name: string;
    price: number;
    color: string,
}

const props = defineProps<{ product: ILastProduvtItemProps }>();
</script>


<style lang="scss" scoped>
.last_product_item {
    display: flex;
    flex-direction: column;
    gap: 20px;

    .image_wrapper {
        position: relative;
        display: flex;
        justify-content: center;
        width: 330px;
        height: 330px;
        border-radius: 30px;

        .bachgraund_shape {
            position: absolute;
            width: 100%;
            height: 100%;
            opacity: 0.3;
            border-radius: 30px;
        }
    }

    img {
        width: 255px;
        height: 358px;
        transform: translateY(-58px);
    }

    .cart_icon_wrapper {
        position: absolute;
        z-index: 20;
        width: 80px;
        height: 80px;
        top: -34px;
        right: -30px;

        &::before {
            content: "";
            display: block;
            border: 2px solid #fff;
            width: 100%;
            height: 100%;
            border-radius: 100%;
            position: absolute;
            border: 4px solid #fff;
            z-index: 30;
        }

        .bachgraund_shape {
            border-radius: 100%;
        }

        img {
            width: 30px;
            height: 30px;
            transform: unset;
        }
    }

    .reyting,
    .name_and_price {
        display: flex;
        justify-content: space-between;
        color: #180202;

        .reyting_text {
            font-size: 16px;
            font-weight: 500;
        }

        .price {
            font-size: 22px;
            font-weight: 400;
        }

        .price {
            font-size: 22px;
            font-weight: 500;
        }
    }
}
</style>