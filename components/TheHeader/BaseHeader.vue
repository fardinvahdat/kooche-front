<template>
  <el-page-header>
    <template #icon
      ><img src="@/assets/images/logo.png" class="logo"
    /></template>

    <template #content>
      <el-input
        class=""
        placeholder="کلمه مورد نظر را وارد کنید... "
        :prefix-icon="Search"
    /></template>
    <template #extra>
      <!-- navigation  -->

      <ul class="navigation">
        <li v-for="(navigation, index) in navigations" :key="index">
          {{ navigation.title }}
        </li>
      </ul>

      <!-- avatar  -->

      <el-dropdown>
        <div class="block">
          <el-avatar :size="50" :src="avatar" />
        </div>
        <template #dropdown>
          <el-dropdown-menu class="avatar-dropdown">
            <el-dropdown-item class="dropdown-item" @click="openLoginDrawer">
              <Icon name="login" />ورود به جساب کاربری</el-dropdown-item
            >
            <el-dropdown-item class="dropdown-item"
              ><Icon name="new-word" />افزودن کلمه جدید</el-dropdown-item
            >
          </el-dropdown-menu>
        </template>
      </el-dropdown>
    </template>
  </el-page-header>
</template>

<script setup>
import Icon from "@/components/TheIcon/Icon.vue";
import { ref } from "vue";
import { Search } from "@element-plus/icons-vue";

//state

const navigations = ref([
  {
    route: "/",
    title: "جست‌وجو",
  },
  {
    route: "/",
    title: "راهنما",
  },
  {
    route: "/",
    title: "درباره",
  },
  {
    route: "/",
    title: "تبلیغات",
  },
]);
const avatar = ref(
  "https://cube.elemecdn.com/3/7c/3ea6beec64369c2642b92c6726f1epng.png"
);
const isLoginDrawwerVisible = useLoginDrawer();

//methods

const openLoginDrawer = () => {
  isLoginDrawwerVisible.value = !isLoginDrawwerVisible.value;
};
</script>

<style>
</style>