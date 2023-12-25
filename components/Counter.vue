<script setup>
import { ref } from 'vue';

const count = ref(0);

function inc(){
  count.value++;
};
function dec(){
  count.value--;
};
</script>
<template>
  <button @click="inc">Increment</button>
  <div>{{ count }}</div>
    <button @click="dec">Decrement</button>
</template>
