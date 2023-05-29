<script setup lang="ts">
    import { type Props } from '@/helpper/types';

    const props = defineProps<Props & { additionalProp?: string }>()
</script>

<template>
    <div>
        <h2>Test</h2>
        <p>First Name: <span>{{ props.firstName }}</span></p>
        <p>Last Name: <span>{{ props.lastName }}</span></p>
        <p>Age: <span>{{ props.age }}</span></p>
        <p>Addprops: <span>{{ props.additionalProp }}</span></p>
    </div>
</template>