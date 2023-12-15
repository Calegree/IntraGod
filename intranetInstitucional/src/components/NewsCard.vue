<script setup>
import { defineProps, ref } from 'vue';
const props = defineProps([
  'NewsImage',
  'NewsTitle',
  'NewsDescription',
  'NewsDate',
])
const imageUrl = ref(props.NewsImage);
</script>

<template>
<div class="card" style="width: 18rem;">
  <img :src="imageUrl" class="card-img-top" alt="...">
  <div class="card-body">
    <h1>{{ props.NewsTitle }}</h1>
    <p class="card-text">{{ props.NewsDescription }}</p>
    <p class="dateText">{{ props.NewsDate }}</p>
    
  </div>
</div>

</template>

<style>
.dateText{
    text-align: right;
}
</style>