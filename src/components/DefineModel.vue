<script setup lang="ts">
    const modelValue = defineModel()
</script>
<template>
    <div>
        <h2>Define Model</h2>
        <input v-model="modelValue" />
        <p>Value: <span>{{ modelValue }}</span></p>
    </div>
</template>