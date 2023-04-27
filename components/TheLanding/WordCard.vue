<template>
  <div class="word-card-item">
    <h3 class="header">{{ data.title }}</h3>
    <p class="content">{{ data.content }}</p>
    <h5 class="author">{{ data.author }}</h5>
    <div class="d-flex w-100 justify-content-between actions">
      <div class="right">
        <span> <Icon name="info" /> گزارش شود</span>
      </div>
      <div class="left">
        <span> <Icon name="dislike" /> حال نکردم </span>
        <span> <Icon name="like" /> حال کردم </span>
      </div>
    </div>
  </div>
</template>

<script setup>
import Icon from "@/components/TheIcon/Icon.vue";
import { defineProps } from "vue";
const props = defineProps({
  data: {
    type: Object,
  },
});
</script>

<style>
</style>