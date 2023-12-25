<script setup>
const page = ref('home')

function view(name) {
  page.value = name;
}
</script>
<template>
  <div style="display: flex;
  justify-content: center;
  flex-direction: column;
  gap: 10px;
  margin-bottom: 30px;
  align-items: center;
  ">
    <a href="#" @click="view('home')">Home</a>
    <a href="#" @click="view('counter')">Counter</a>
  </div>
  <div style="display: flex;
  justify-content: center;
  flex-direction: column;
  gap: 10px;
  margin-bottom: 30px;
  align-items: center;
  ">
<HomeWelcome v-if="page ==='home'"/>
<Counter v-if="page === 'counter'"/>
  </div>
</template>
