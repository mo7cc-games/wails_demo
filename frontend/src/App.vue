<script setup>
import { ref } from "vue";
import HelloWorld from "./components/HelloWorld.vue";
import { AddNumbers } from "../wailsjs/go/main/App";

const num1 = ref(0);
const num2 = ref(0);
const result = ref(0);

function calculate() {
  // 调用Go后端的AddNumbers方法
  AddNumbers(num1.value, num2.value).then((res) => {
    console.log("计算结果:", res);
    result.value = res;
  });
}
</script>

<template>
  <img id="logo" alt="Wails logo" src="./assets/images/logo-universal.png" />
  <HelloWorld />

  <div class="calculator">
    <h3>简单计算器</h3>
    <input type="number" v-model="num1" />
    <span>+</span>
    <input type="number" v-model="num2" />
    <button @click="calculate">计算</button>
    <p>结果: {{ result }}</p>
  </div>
</template>

<style>
#logo {
  display: block;
  width: 50%;
  height: 50%;
  margin: auto;
  padding: 10% 0 0;
  background-position: center;
  background-repeat: no-repeat;
  background-size: 100% 100%;
  background-origin: content-box;
}

/* 添加一些简单样式 */
.calculator {
  margin-top: 20px;
  padding: 10px;
  border: 1px solid #ccc;
  border-radius: 5px;
}
.calculator input {
  width: 80px;
  margin: 0 5px;
}
.calculator button {
  margin: 0 5px;
  padding: 0 10px;
}
</style>
