<script setup>
  defineProps({
    imgSource: String,
    textArticle: String,
  });
</script>

<template>
  <div class="container">
    <img height="128" width="128" :src="imgSource" alt="image" />
    <p>{{ textArticle }}</p>
  </div>
</template>



<style scoped>
.container {
  display: flex;
  flex-direction: column;
  align-items: center;
  border: 2px solid black;
  margin: 20px;
  padding: 10px;
  border-radius: 5px;
}
</style>
