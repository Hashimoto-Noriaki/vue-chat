<template>
  <div class="container welcome">
    <p>ようこそ</p>
    <div v-if="shouldShowLoginForm">
      <LoginForm />
      <p class="change-form">初めての方は<span @click="shouldShowLoginForm = false">こちら</span>をクリック</p>
    </div>
    <div v-if="!shouldShowLoginForm">
      <SignupForm />
      <p class="change-form">アカウントをお持ちの方は<span @click="shouldShowLoginForm = true"></span></p>
    </div>
  </div>
</template>

<script>
import LoginForm from '../components/LoginForm.vue'
import SignupForm from '../components/SignupForm.vue'
export default {
  components: { LoginForm, SignupForm },
  data () {
    return {
      shouldShowLoginForm: true
    }
  }
}
</script>

<style>
 .container {
    text-align: center; /* 追加: テキストを中央に揃える */
  }

  .welcome form {
    width: 300px;
    margin: 20px auto;
  }
  .welcome label {
    display: block;
    margin: 20px 0 10px;
  }
  .welcome input {
    width: 100%;
    padding: 12px 20px;
    margin: 8px auto;
    border-radius: 4px;
    border: 1px solid #eee;
    outline: none;
    box-sizing: border-box;
  }
  .welcome span{
    font-weight: bold;
    text-decoration: underline;
    cursor: pointer;
  }
  .welcome button {
    margin: 20px auto;
  }

  .change-form {
    font-size: 14px;
    margin: 10px;
  }
</style>
