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

button.main {
  height: 70px;
  padding: 0 70px;
  background: linear-gradient(0deg, #7db945, #7db945);
  border-radius: 10px;
  font-family: "Rotonda", sans-serif;
  font-weight: bold;
  font-size: 22px;
  line-height: 36px;
  color: white;
  border: none;
  cursor: pointer;
}
</style>
