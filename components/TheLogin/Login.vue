<template>
  <div class="login-form">
    <h2 class="header">ورود به وبسایت</h2>
    <form
      action=""
      class="login-username"
      @submit.prevent="handleUsernameLogin"
      v-if="loginMode === 1"
    >
      <input
        type="text"
        placeholder="نام کاربری"
        v-model="userNameLogin.username"
      />
      <input
        type="password"
        placeholder="رمز عبور"
        v-model="userNameLogin.password"
      />
      <button type="">ورود</button>
      <div class="actions d-flex">
        <button type="button" @click="loginMode = 2">
          <Icon name="mobile" /> ورود از طریق شماره موبایل
        </button>
        <button type="button"><Icon name="gmail" /> ورود از طریق جیمیل</button>
      </div>
    </form>
    <form
      action=""
      class="login-username"
      @submit.prevent="handleUsernameLogin"
      v-if="loginMode === 2"
    >
      <input
        type="number"
        placeholder="شماره موبایل"
        v-model="phoneNumberLogin.phoneNumber"
      />
      <input
        type="password"
        placeholder="رمز عبور"
        v-model="phoneNumberLogin.password"
      />
      <button type="">ورود</button>
      <div class="actions d-flex">
        <button type="button" @click="loginMode = 1">
          <Icon name="user" /> ورود از طریق نام کاربری
        </button>
        <button type="button"><Icon name="gmail" /> ورود از طریق جیمیل</button>
      </div>
    </form>
  </div>
</template>

<script setup>
import Icon from "@/components/TheIcon/Icon.vue";
import { ref } from "vue";

//state

const loginMode = ref(1);
const userNameLogin = ref({
  username: "",
  password: "",
});
const phoneNumberLogin = ref({
  phoneNumber: "",
  password: "",
});

//methods

const handleUsernameLogin = () => {
  console.log(userNameLogin.value);
};
</script>

<style>
</style>