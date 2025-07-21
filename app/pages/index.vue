<template>
  <div>
    <HelloWorld :person="person" />
  </div>
</template>

<script setup lang="ts">
import HelloWorld from '~/components/HelloWorld.vue';

const person : {name:string; age: number; hobbies: string[]} = {
  name: 'Greg',
  age: 33,
  hobbies :['velo', 'tech', 'sport']
}
</script>
