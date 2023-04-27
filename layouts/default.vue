<template>
  <BaseHeader />
  <el-container class="d-flex">
    <el-main>
      <NuxtPage />
    </el-main>
  </el-container>
  <el-drawer v-model="isLoginDrawwerVisible" :show-close="false">
    <template #header="{ close }">
      <span @click="close" class="close-icon">
        <Icon name="close" />
      </span>
    </template>
    <Login />
  </el-drawer>
</template>

<script setup>
import BaseHeader from "@/components/TheHeader/BaseHeader.vue";
import Login from "@/components/TheLogin/Login.vue";
import Icon from "@/components/TheIcon/Icon.vue";
import { ref } from "vue";

//state

const isLoginDrawwerVisible = useLoginDrawer();
</script>

<style>
</style>