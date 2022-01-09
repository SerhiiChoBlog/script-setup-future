<script setup lang="ts">
import OptionsApiModal from './components/OptionsApiModal.vue'
import CompositionApiModal from './components/CompositionApiModal.vue'
import ScriptSetupModal from './components/ScriptSetupModal.vue'
import Counter from './components/Counter.vue'
import Spinner from './components/Spinner.vue'
</script>

<template>
    <div class="border p-5 m-4 rounded">
        <h1 class="text-xl">Modals examples</h1>

        <OptionsApiModal />
        <CompositionApiModal />
        <ScriptSetupModal />
    </div>

    <div class="border p-5 m-4 rounded">
        <h1 class="text-xl">Click on the number</h1>
        <Counter />
    </div>

    <div class="border p-5 m-4 rounded">
        <h1 class="text-xl mb-4">Spinner example</h1>
        <Spinner />
    </div>
</template>