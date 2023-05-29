<script setup lang="ts">
    const props = defineProps(['id', 'name'])
    const emit = defineEmits<{
        foo: [id: number]
        bar: [name: string, ...rest: any[]]
    }>()
    function foo() {
        emit('foo', props.id)
    }
    function bar() {
        emit('bar', props.name, 'test 1', 'test 2', 'test 3')
    }
</script>

<template>
    <div>
        <h2>More Ergonomic defineEmits</h2>
        <button @click="foo">Click Me Foo</button>
        <button @click="bar">Click Me Bar</button>
    </div>
</template>