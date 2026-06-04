<template>
  <div class="app-container">
    <DiscordLogo />
    
    <main class="page">
      <section class="login-card" aria-label="Discord login card">
        <LoginForm />
        <QrCodePanel />
      </section>
    </main>
  </div>
</template>

<script setup>
// 引入拆分好的三個元件
import DiscordLogo from './components/DiscordLogo.vue'
import LoginForm from './components/LoginForm.vue'
import QrCodePanel from './components/QrCodePanel.vue'
</script>

<style scoped>
.page {
  min-height: 100vh;
  display: grid;
  place-items: center;
  padding: 24px;
}

.login-card {
  width: min(784px, 100%);
  min-height: 410px;
  background: var(--card);
  border-radius: 8px;
  box-shadow: 0 2px 10px var(--card-shadow);
  display: grid;
  grid-template-columns: 3fr 2fr;
  gap: 28px;
  padding: 32px;
}

@media (max-width: 830px) {
  .page {
    padding: 16px;
  }

  .login-card {
    width: 100%;
    max-width: none;
    min-height: auto;
    grid-template-columns: 1fr;
    gap: 0;
    padding: 24px;
    margin-top: 28px;
  }
}
</style>