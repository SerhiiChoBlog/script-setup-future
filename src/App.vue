<script setup lang="ts">
import OptionsApiModal from './components/OptionsApiModal.vue'
import CompositionApiModal from './components/CompositionApiModal.vue'
import ScriptSetupModal from './components/ScriptSetupModal.vue'
import Counter from './components/Counter.vue'
</script>

<template>
    <OptionsApiModal />
    <CompositionApiModal />
    <ScriptSetupModal />

    <div class="border p-5 m-4 rounded">
        <h1 class="text-xl">Click on the number</h1>
        <Counter />
    </div>
</template>