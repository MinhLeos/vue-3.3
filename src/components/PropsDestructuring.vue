<script setup lang="ts">
    const { count: number = 1, title: demo = 'Demo' } = defineProps(['count', 'title'])
</script>
<template>
    <div>
        <h2>Props Destructuring</h2>
        <p>{{ demo }} - {{ number }}</p>
    </div>
</template>