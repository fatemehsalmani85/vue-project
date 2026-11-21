
<script setup>
import { ref } from 'vue'

const count = ref(0)

function increase() {
  count.value++
}

function decrease() {
  if (count.value > 0) {
    count.value--
  }
}

function reset() {
  count.value = 0
}
</script>

<template>
  <div class="container">
    <div class="counter-box">
      <h1>شمارنده من</h1>
      <p>عدد مورد نظر خود را مدیریت کنید</p>

      <div class="number">
        {{ count }}
      </div>

      <div class="buttons">
        <button class="plus" @click="increase">
          +
        </button>

        <button class="minus" @click="decrease">
          -
        </button>

        <button class="reset" @click="reset">
          صفر کردن
        </button>
      </div>
    </div>
  </div>
</template>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: Tahoma, sans-serif;
  background: #eaf4ff;
}

.container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  background: linear-gradient(135deg, #dbeafe, #eff6ff);
}

.counter-box {
  width: 340px;
  padding: 35px;
  text-align: center;
  background: white;
  border-radius: 25px;
  box-shadow: 0 10px 35px rgba(37, 99, 235, 0.15);
}

h1 {
  color: #1e40af;
  margin-bottom: 12px;
}

p {
  color: #64748b;
  font-size: 13px;
}

.number {
  font-size: 75px;
  font-weight: bold;
  color: #2563eb;
  margin: 30px 0;
}

.buttons {
  display: flex;
  justify-content: center;
  gap: 10px;
  flex-wrap: wrap;
}

button {
  border: none;
  padding: 12px 20px;
  border-radius: 12px;
  font-size: 20px;
  cursor: pointer;
  transition: 0.3s;
}

button:hover {
  transform: translateY(-3px);
}

.plus {
  background: #2563eb;
  color: white;
}

.minus {
  background: #60a5fa;
  color: white;
}

.reset {
  background: #dbeafe;
  color: #1e40af;
  font-size: 14px;
}
</style>
