<script setup>
const props = defineProps({
    title: String,
    description: String,
    skills: Array
  });
  </script>

<template>
    <div class="bg-white m-6 p-2">
    <h1 class="text-center font-medium text-lg">{{ title }}</h1>
    <p class="text-justify font-light">{{ description }}</p>
    <ul>
      <li v-for="(skill, index) in skills" :key="index" class="border my-2 font-light py-1 pl-2 cursor-pointer border-blue-200">{{ skill }}</li>
    </ul>
  </div>
</template>

<style lang="css"></style>