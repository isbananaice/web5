<template>
  <aside class="qr-panel" aria-label="Scan QR code">
    <div class="qr-box">
      <img class="qr-image" src="/asset/QRcode.png" alt="Discord QR code">
      <div class="qr-center-icon" aria-hidden="true">
        <img src="/asset/smallicon.png" alt="icon">
      </div>
    </div>
    <h2>使用 QR Code 登入</h2>
    <p>
      用 <strong>Discord</strong> 行動應用程式 對此掃描，<br>
      就能立即登入。
      <a class="passkey-login" href="https://www.youtube.com/watch?v=b8fKDXWH-kI">或者，使用密碼金鑰登入</a>
    </p>
  </aside>
</template>

<style scoped>
.qr-panel {
  text-align: center;
  display: grid;
  align-content: center;
  gap: 35px;
  padding-left: 28px;
}

.qr-box {
  width: 176px;
  height: 176px;
  margin: -20px auto 0;
  border-radius: 8px;
  background: #ffffff;
  padding: 12px;
  overflow: hidden;
  position: relative;
}

.qr-image {
  width: 100%;
  height: 100%;
  object-fit: contain;
  display: block;
  transform: scale(1.12);
  transform-origin: center;
}

.qr-center-icon {
  position: absolute;
  width: 40px;
  height: 40px;
  left: 50%;
  top: 50%;
  transform: translate3d(-50%, -50%, 0);
  border-radius: 50%;
  background: var(--bg-main);
  border: 4px solid #ffffff;
  display: grid;
  place-items: center;
  padding: 0;
  overflow: hidden;
  z-index: 2;
}

.qr-center-icon img {
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
  width: 130%;
  height: 130%;
  display: block;
  object-fit: contain;
}

.qr-panel h2 {
  margin: 0;
  font-size: 23px;
  line-height: 1.15;
}

.qr-panel p {
  margin: -25px 0 0;
  color: #ffffff;
  line-height: 1.45;
  font-size: 14px;
}

.qr-panel strong {
  color: #ffffff;
  font-weight: 600;
}

.passkey-login {
  display: block;
  margin-top: 6px;
  font-size: 13px;
  color: #7cc9ff;
  text-decoration: none;
}

.passkey-login:hover {
  text-decoration: underline;
}

/* RWD: 當畫面小於 830px 時，隱藏 QR Code 區塊 */
@media (max-width: 830px) {
  .qr-panel {
    display: none;
  }
}
</style>