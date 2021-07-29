<template>
  <div id="app">
    <router-view />
  </div>
</template>

<style lang="scss">
@font-face {
  font-family: "Rotonda";
  src: url("./assets/fonts/RotondaC.eot");
  src: url("./assets/fonts/RotondaC.eot?#iefix") format("embedded-opentype"),
    url("./assets/fonts/RotondaC.woff") format("woff"),
    url("./assets/fonts/RotondaC.ttf") format("truetype");
  font-weight: normal;
  font-style: normal;
}

@font-face {
  font-family: "Rotonda";
  src: url("./assets/fonts/RotondaC-Bold.eot");
  src: url("./assets/fonts/RotondaC-Bold.eot?#iefix")
      format("embedded-opentype"),
    url("./assets/fonts/RotondaC-Bold.woff") format("woff"),
    url("./assets/fonts/RotondaC-Bold.ttf") format("truetype");
  font-weight: bold;
  font-style: normal;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  background: #f7f7f7;
}

// Текстовые стили
h2 {
  font-family: "Rotonda", sans-serif;
  font-weight: bold;
  font-size: 36px;
  line-height: 46px;
  color: #26303b;
  max-width: 640px;
}

h4 {
  font-family: "Rotonda", sans-serif;
  font-size: 16px;
  line-height: 24px;
  color: #26303b;
  font-weight: bold;
}

p {
  font-family: "Rotonda", sans-serif;
  font-size: 16px;
  line-height: 24px;
  color: #26303b;
}

button {
  background: linear-gradient(0deg, #7db945, #7db945);
  font-family: "Rotonda", sans-serif;
  font-weight: bold;
  color: white;
  border: none;
  cursor: pointer;

  &.main {
    height: 70px;
    padding: 0 70px;
    font-size: 22px;
    line-height: 36px;
    border-radius: 10px;
  }

  &.secondary {
    padding: 15px 40px;
    font-size: 16px;
    border-radius: 7px;
  }
}

input {
  font-size: 16px;
  padding: 15px;
  outline: none;
  border: none;
  border-radius: 7px;
  color: #26303b;
  background: #f3f4f6;
  font-family: "Rotonda", sans-serif;
}

@media (max-width: 950px) {
  h2 {
    font-size: 26px;
    line-height: 32px;
  }

  p {
    font-size: 14px;
    line-height: 22px;
  }
}
</style>
