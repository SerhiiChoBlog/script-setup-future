<template>
    <div
        v-if="isOpen"
        class="bg-white shadow-lg absolute p-10 border-2 top-[50%] left-[50%] translate-x-[-50%] translate-y-[-50%] rounded-md"
    >
        <h1 class="text-center text-xl">Contact modal</h1>
        <button
            @click="closeContactModal"
            class="px-3 py-2 rounded-md bg-red-700 text-white m-6"
        >Close modal</button>
    </div>
    <button
        @click="openContactModal"
        class="m-4 px-3 py-2 rounded-md bg-green-700 text-white"
    >Open modal</button>
</template>

<script lang="ts">
import { ref, defineComponent, onMounted } from 'vue'

export default defineComponent({
    setup() {
        const isOpen = ref(false)

        function openContactModal(): void {
            isOpen.value = true
        }

        function closeContactModal(): void {
            isOpen.value = false
        }

        onMounted(() => {
            window.addEventListener('keydown', e => {
                if (e.key === 'Escape') {
                    closeContactModal()
                }
            })
        })

        return {
            isOpen,
            openContactModal,
            closeContactModal,
        }
    },
})
</script>