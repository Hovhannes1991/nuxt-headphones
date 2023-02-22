<template>
    <div class="latest_collection">
        <h2>
            Our Latest Collention
        </h2>

        <div v-if="images.length" class="slider flex-center">
            <div class="previous_image">
                <img @click="changeSlide(current_slide - 1)" src="icons/to-left.svg" alt="previous image">
            </div>

            <div class="slider_content">
                <div class="left_image flex-center" key="111">
                    <img v-if="current_slide > 0" :src="'images/' + images[current_slide - 1]" alt="previous image" key="1">
                    <img v-else :src="'images/' + images[images.length - 1]" alt="previous image" key="2">
                </div>

                <div class="center_image flex-center" key="222">
                    <img :src="'images/' + images[current_slide]" alt="current image" key="3">
                </div>

                <div class="right_image flex-center" key="333">
                    <img v-if="current_slide < images.length - 1" :src="'images/' + images[current_slide + 1]"
                        alt="next image" key="4">
                    <img v-else :src="'images/' + images[0]" alt="next image" key="5">
                </div>
            </div>

            <div class="next_image">
                <img @click="changeSlide(current_slide + 1)" src="icons/to-right.svg" alt="next image">
            </div>
        </div>
    </div>
</template>

<script setup lang="ts">
const images = ref(['headphone-red.png', 'headphone-orange.png', 'headphone-blue.svg', 'headphone-grey.png', 'headphone-red.png', 'headphone-orange.png', 'headphone-blue.svg', 'headphone-grey.png'])
const current_slide = ref(1);

const changeSlide = (value: number) => {
    console.log(value);
    if (value < 0) value = images.value.length - 1;
    else if (value > images.value.length - 1) value = 0;
    current_slide.value = value;

}
</script>

<style lang="scss" scoped>
.latest_collection {
    padding-top: 130px;
    background-color: #fff;

    h2 {
        text-align: center;
    }
}

.slider {
    gap: 30px;
    margin: 50px auto 0 auto;

    .previous_image,
    .next_image {
        cursor: pointer;
    }

    .slider_content {
        display: flex;
        align-items: flex-end;

        .left_image,
        .right_image {
            border-radius: 30px;
            border: 1px solid rgba(125, 117, 117, 0.3);
            padding: 50px;

            img {
                width: 200px;
                height: 200px;
            }
        }

        .left_image {
            transform: translateX(50px);
        }

        .right_image {
            transform: translateX(-50px);
        }

        .center_image {
            z-index: 10;
            background-color: #fff;
            max-width: 40vw;
            max-height: 37vw;
            border-radius: 30px;
            box-shadow: 0px 21px 88px rgba(126, 118, 118, 0.2);
            padding: 50px;

            img {
                width: 350px;
                height: 350px;
            }
        }
    }
}
</style>