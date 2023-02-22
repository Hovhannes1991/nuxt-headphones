<template>
    <div>
        <img v-for="n in reyting" src="icons/star.svg" alt="reyting">
        <img v-for="n in empty_icons" src="icons/star-empty.svg" alt="reyting">
    </div>
</template>

<script setup lang="ts">
const props = defineProps<{reyting: number}>();

let reyting = Math.round(props.reyting);
reyting = reyting > 5 ? 5 : reyting < 0 ? 0 : reyting;

const empty_icons = 5 - reyting;
</script>