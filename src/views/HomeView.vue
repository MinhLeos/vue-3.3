<script setup lang="ts">
  import { ref } from 'vue'
  import TestVue from '../components/TestVue.vue'
  import  GenericComponent from '../components/GenericComponent.vue';
  import  MoreDefineEmits from '../components/MoreDefineEmits.vue';
  import  DefineSlot from '../components/DefineSlot.vue';
  import  PropsDestructuring from '../components/PropsDestructuring.vue';
  import  DefineModel from '../components/DefineModel.vue';
  
  const lastName = ref('Le')
  const age = ref(18)
  const idString = ref('string')
  const firstName = ref('Minh')
  const idNumber = ref(18)
  const listNames = ref(['Minh', 'Quang', "Le"])
  const listItems = ref([
    {
      id: '1',
      title: 'Vue 3.1'
    },
    {
      id: '2',
      title: 'Vue 3.2'
    },
    {
      id: '3',
      title: 'Vue 3.3'
    }
  ])

  function handleFoo(value: number) {
    console.log('Foo: ', value)
  }
  function handleBar(name: any, ...value: string[]) {
    console.log('Bar name: ', name)
    console.log('Bar value: ', value)
  }
  const modelValue = ref('')
</script>

<template>
  <main>
    <!-- Imported and Complex Types Support in Macros:  -->
    <TestVue :first-name="firstName" :last-name="lastName" :age="age" additionalProp="additionalProp"/>

    <TestVue :first-name="firstName" :last-name="lastName" :age="age" />

    <!-- Generic Component -->
    <!-- <GenericComponent :id="idString" :list="listItems"/> -->
    <!-- <GenericComponent :id="idNumber" :list="listItems"/> -->

    <!-- More Ergonomic defineEmits -->
    <!-- <MoreDefineEmits :id="idNumber" :name="firstName" @foo="handleFoo" @bar="handleBar"/>
    <p>------------------</p>
    <MoreDefineEmits :id="idNumber" :name="listNames" @foo="handleFoo" @bar="handleBar"/> -->

    <!-- Define Slot -->
    <!-- <DefineSlot>
      <template v-slot="slotProps">
          <p>{{ slotProps.title }} - {{ slotProps.des }}</p>
      </template>
      <template #demo="demoProps">
          <p>{{ demoProps.title }}</p>
      </template>
    </DefineSlot> -->

    <!-- Props Destructuring -->
    <!-- <PropsDestructuring :count="10" />
    <PropsDestructuring title="Destructuring" /> -->

    <!-- Define Model -->
    <!-- <DefineModel v-model="modelValue" /> -->
    <hr />
  </main>
</template>
