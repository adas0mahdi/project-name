<script setup>
const page = ref('')

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
    <a style=" color: rgb(5, 142, 96); text-decoration:none;" href="#" @click="view('home')">Home</a>
    <a style=" color: rgb(5, 142, 96); text-decoration:none;" href="#" @click="view('counter')">Counter</a>
  </div>
  <div style="display: flex;
  justify-content: center;
  flex-direction: column;
  gap: 10px;
  margin-bottom: 30px;
  align-items: center;
  ">
<LazyHomeWelcome v-if="page ==='home'"/>
<LazyCounter v-if="page === 'counter'"/>
  </div>
</template>
