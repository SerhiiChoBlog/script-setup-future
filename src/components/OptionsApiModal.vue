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
        class="m-4 px-3 py-2 rounded-md bg-gray-700 text-white"
    >Open modal</button>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
    data() {
        return {
            isOpen: false,
        }
    },

    mounted() {
        window.addEventListener('keydown', e => {
            if (e.key === 'Escape') {
                this.closeContactModal()
            }
        })
    },

    methods: {
        openContactModal(): void {
            this.isOpen = true
        },
        closeContactModal(): void {
            this.isOpen = false
        },
    },
})
</script>