<script setup>
import { ref } from "vue";
import { my_project_backend } from "declarations/my_project_backend/index";
let greeting = ref("");

async function handleSubmit(e) {
  e.preventDefault();
  const target = e.target;
  const name = target.querySelector("#name").value;
  await my_project_backend.greet(name).then((response) => {
    greeting.value = response;
  });
}
</script>

<template>
  <img src="/logo2.svg" alt="DFINITY logo" class="icp-img" />
  <header>
    <h1 id="greeting">Kacper Kleist</h1>
    <h2>Student</h2>
  </header>
</template>

<style scoped>
header {
  text-align: center;
  margin-top: 16px;
  padding: 85px 20px;
  background-color: rgba(104, 255, 42, 1);
  background-image: linear-gradient(301deg, rgba(110, 255, 50, 1) 0%, rgb(43, 59, 36) 100%);
  color: #fff;
  border: 7px #121212 solid;
  border-radius: 48px;
  max-width: 60%;
  max-height: 250px;
  height: 100%;
  width: 100%;
  -webkit-box-shadow: 0px 0px 32px 6px rgba(104, 255, 42, 1);
  -moz-box-shadow: 0px 0px 32px 6px rgba(104, 255, 42, 1);
  box-shadow: 0px 0px 32px 6px rgba(102, 255, 42, 0.775);
}
h1 {
  font-size: 4rem;
  margin-bottom: 10px;
}
h2 {
  font-size: 3rem;
  color: #a3cfff;
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

.icp-img {
  margin-top: 25px;
  max-width: 450px;
  width: 100%;
}
</style>