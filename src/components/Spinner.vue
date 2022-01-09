<script setup lang="ts">
interface Props {
    center?: boolean
}

withDefaults(defineProps<Props>(), {
    center: false
})
</script>

<template>
    <div class="text-center" :class="{ 'center-the-spinner': center }">
        <div class="spinner-border text-secondary" role="status"></div>
    </div>
</template>

<style lang="scss" scoped>
.center-the-spinner {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
}
</style>