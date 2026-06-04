<template>
  <a class="page-logo" href="#" aria-label="Discord home">
    <img src="/asset/131c318dd45b7aa4.svg" alt="Discord">
  </a>
</template>

<style scoped>
.page-logo {
  position: fixed;
  top: 48px;
  left: 48px;
  z-index: 5;
  display: inline-flex;
}

.page-logo img {
  width: 124px;
  height: auto;
  display: block;
}

@media (max-width: 830px) {
  .page-logo {
    top: 24px;
    left: 24px;
  }
  .page-logo img {
    width: 108px;
  }
}
</style>