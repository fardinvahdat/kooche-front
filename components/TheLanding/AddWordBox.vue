<template>
  <div class="add-word-box">
    <div class="d-flex header">
      <span> فرهنگ کوچه را شما می‌نویسید! </span>
      <img src="../../assets/images/cat-typing.png" alt="" />
    </div>
    <button type="button" class="primary add-new">افزودن کلمه</button>
  </div>
</template>

<script setup>
import { ref } from "vue";
const catTypeImage = ref("../../assets/images/cat-typing.png");
</script>

<style>
</style>