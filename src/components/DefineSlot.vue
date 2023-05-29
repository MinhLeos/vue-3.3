<template>
    <div>
        <h2>Define Slot</h2>
        <slot title="Slot Default" des="Description"></slot>
        <div>
            <slot name="demo" title="Name Slot"></slot>
        </div>
    </div>
</template>
<script setup lang="ts">
    defineSlots<{
        default?: (props: { title: string, des: string }) => any
        demo?: (props: { title: string }) => any
    }>()
</script>