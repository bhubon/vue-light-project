<script setup>

import { ref, reactive } from 'vue';

const lightIcon = {
  lightOnIcon: '//img.icons8.com/?size=512&id=12244&format=png',
  lightOffIcon: '//img.icons8.com/?size=512&id=75&format=png',
}

const lightOne = ref(true);
const lightTwo = ref(true);
const lightThree = ref(true);


</script>

<template>
  <section class="container mx-auto flex items-center flex-col">
    <h1 class="text-center text-2xl py-10">Assignment</h1>
    <p class="p-5">Make These Buttons Work</p>
    <div class="flex justify-between space-x-6">
      <div class="p-10 border w-96 flex flex-col space-y-5">
        <button @click="lightOne = !lightOne" class="text-white font-bold py-2 px-4 rounded"
          :class="lightOne ? 'bg-blue-500 hover:bg-blue-700' : 'bg-gray-500 hover:bg-gray-700'">
          Light 1 {{ lightOne ? 'On' : 'Off' }}
        </button>
        <button @click="lightTwo = !lightTwo" class="text-white font-bold py-2 px-4 rounded"
          :class="lightTwo ? 'bg-blue-500 hover:bg-blue-700' : 'bg-gray-500 hover:bg-gray-700'">
          Light 2 {{ lightTwo ? 'On' : 'Off' }}
        </button>
        <button @click="lightThree = !lightThree" class="text-white font-bold py-2 px-4 rounded"
          :class="lightThree ? 'bg-blue-500 hover:bg-blue-700' : 'bg-gray-500 hover:bg-gray-700'">
          Light 3 {{ lightThree ? 'On' : 'Off' }}
        </button>
      </div>
      <div class="p-10 border w-96 flex flex-col space-y-5">
        <img class="w-20" :src="lightOne ? lightIcon.lightOnIcon : lightIcon.lightOffIcon" alt="">
        <img class="w-20" :src="lightTwo ? lightIcon.lightOnIcon : lightIcon.lightOffIcon" alt="">
        <img class="w-20" :src="lightThree ? lightIcon.lightOnIcon : lightIcon.lightOffIcon" alt="">
      </div>
    </div>
  </section>
</template>

<style scoped></style>