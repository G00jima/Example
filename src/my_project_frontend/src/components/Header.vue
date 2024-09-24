<script setup>
import { ref } from 'vue';
import { my_project_backend } from 'declarations/my_project_backend/index';
let greeting = ref('');

async function handleSubmit(e) {
  e.preventDefault();
  const target = e.target;
  const name = target.querySelector('#name').value;
  await my_project_backend.greet(name).then((response) => {
    greeting.value = response;
  });
}
</script>

<template>
    <img src="/logo2.svg" alt="DFINITY logo" class="icp-img" />
    <form action="#" @submit="handleSubmit">
      <label for="name">Enter your name: &nbsp;</label>
      <input id="name" alt="Name" type="type" />
      <button type="submit">Click Me!</button>
      <header>
        <h1 id="greeting">{{ greeting }}</h1>
        <h2>Aspirujący Gitarzysta</h2>
      </header>
    </form>
</template>

<style scoped>
header {
  text-align: center;
  margin-top: 16px;
  padding: 85px 20px;
  background: linear-gradient(to right, #ff5100, #ff0000);
  color: #050505;
  border-radius: 48px;
  max-width: 1200px;
  width: 100%;
  -webkit-box-shadow: 0px 0px 32px 6px rgb(255, 0, 0);
  -moz-box-shadow: 0px 0px 32px 6px rgb(255, 0, 0);
  box-shadow: 0px 0px 32px 6px rgb(255, 0, 0);
}
h1 {
  font-size: 4rem;
  margin-bottom: 10px;
}
h2 {
  font-size: 2rem;
  color: #161616;
}
p {
  font-size: 1.2rem;
  max-width: 600px;
  margin: 20px auto 0;
}

form {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  gap: 16px;
}
.template {
  margin-top: 16px;
 
}
</style>
