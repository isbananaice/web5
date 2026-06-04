<template>
  <div class="form-panel">
    <h1>歡迎回來！</h1>
    <p class="subtitle">我們很高興又見到你！</p>

    <form class="login-form" action="#" method="post" @submit.prevent="handleLogin">
      <label for="email">電子郵件地址或手機號碼 <span class="required">*</span></label>
      <input id="email" name="email" type="text" autocomplete="username" required>

      <label for="password">密碼 <span class="required">*</span></label>
      <input id="password" name="password" type="password" autocomplete="current-password" required>

      <a class="forgot" href="https://www.youtube.com/watch?v=NPU_ery8M0I">忘記你的密碼？</a>

      <button type="submit">登入</button>
    </form>

    <p class="register">需要一個帳號嗎？ <a href="https://www.youtube.com/watch?v=0WA2NX4kPSI">註冊</a></p>
  </div>
</template>

<script setup>
const handleLogin = () => {
  window.location.href = 'https://www.youtube.com/watch?v=h0djuhl97Kw';
}
</script>

<style scoped>
.form-panel h1 {
  margin: 0 0 6px;
  text-align: center;
  color: #ffffff;
  font-size: 24px;
  font-weight: 700;
}

.subtitle {
  margin: 0 0 22px;
  text-align: center;
  color: var(--muted);
  font-size: 16px;
}

.login-form {
  display: grid;
  gap: 10px;
}

.login-form label {
  font-size: 13px;
  font-weight: 400;
  color: #ffffff;
  letter-spacing: 0.02em;
  text-transform: uppercase;
}

.required {
  color: #ed4245;
}

.login-form input {
  width: 100%;
  height: 40px;
  border-radius: 4px;
  border: 1px solid var(--input-border);
  background: var(--input-bg);
  color: #f2f3f5;
  padding: 0 12px;
  font-size: 15px;
}

.login-form input:focus {
  outline: none;
  border-color: var(--brand);
  box-shadow: 0 0 0 2px rgba(88, 101, 242, 0.35);
}

.forgot, .register a {
  color: #7cc9ff;
  text-decoration: none;
}

.forgot:hover, .register a:hover {
  text-decoration: underline;
}

.forgot {
  margin: 2px 0 6px;
  font-size: 14px;
}

.login-form button {
  margin-top: 6px;
  height: 44px;
  width: 100%;
  border: 0;
  border-radius: 4px;
  background: var(--bg-main);
  color: #ffffff;
  font-size: 15px;
  font-weight: 600;
  cursor: pointer;
  transition: background-color 0.15s ease;
}

.login-form button:hover {
  background: var(--brand-hover);
}

.login-form button:active {
  background: var(--brand-active);
}

.register {
  margin: 14px 0 0;
  color: var(--muted);
  font-size: 14px;
}
</style>