<script setup lang="ts" generic="T extends string | number, U extends Item">
    import { type Item } from '../helpper/types'

    const props = defineProps<{ 
        id: T
        list: U[]
    }>()
    console.log('props', props)
</script>
<template>
    <div>
        <h2>Generic Component</h2>
        <p>Type Of T: <span style="color: red;">{{( typeof id)}}</span></p>
        <ul>
            <li v-for="item in list" :key="item.id">{{ item.id }} - {{ item }}</li>
        </ul>
    </div>
</template>