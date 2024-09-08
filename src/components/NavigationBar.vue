<script setup>
import ToggleDdarkMode from "./ToggleDarkMode.vue";

defineProps({
    title: String,
});
</script>

<template>
    <div class="items-center flex flex-col itmes-center gap-6">
        <h1 class="text-center dark:text-[#FFDE4D] text-5xl font-bold">{{ title }}</h1>
        <ToggleDdarkMode />
    </div>
</template>

<style scoped></style>
