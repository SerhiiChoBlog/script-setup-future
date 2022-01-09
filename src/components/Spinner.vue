<script setup lang="ts">
interface Props {
    center?: boolean
}

withDefaults(defineProps<Props>(), {
    center: false
})
</script>

<template>
    <div
        style="border-top-color:transparent"
        class="w-10 h-10 border-4 border-blue-400 border-solid rounded-full animate-spin"
        :class="{ 'center-the-spinner': center }"
    ></div>
</template>

<style scoped>
.center-the-spinner {
    position: absolute;
    top: 50%;
    left: 50%;
}
</style>