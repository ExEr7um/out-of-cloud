<template>
  <div class="popup-bg">
    <div class="popup">
      <h2 v-if="isSent">Спасибо!</h2>
      <form @submit.prevent="send" v-else>
        <div class="input-container">
          <p><label for="email">Ваш Email</label></p>
          <input
            type="email"
            required
            id="email"
            placeholder="you@example.com"
            v-model="form.email"
          />
        </div>
        <button type="submit" class="secondary">Отправить</button>
      </form>
      <div class="close" @click="$emit('close')">✕</div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      form: {
        email: "",
      },
      isSent: false,
    };
  },
  methods: {
    async send() {
      const user = await this.form.email;
      console.log(user);
      this.isSent = true;
    },
  },
};
</script>

<style lang="scss" scoped>
.popup-bg {
  position: fixed;
  width: 100%;
  height: 100%;
  background: rgba($color: #000000, $alpha: 0.15);
  top: 0;
  left: 0;
  backdrop-filter: blur(3px);
  display: flex;
  align-items: center;
  justify-content: center;

  .popup {
    position: relative;
    background: white;
    border-radius: 10px;
    padding: 50px 40px 30px;

    h2 {
      margin: 50px;
    }

    form {
      display: flex;
      flex-direction: column;
      align-items: center;

      .input-container {
        margin-bottom: 30px;

        input {
          margin-top: 5px;
          width: 300px;
        }
      }
    }

    .close {
      position: absolute;
      top: 20px;
      right: 20px;
      color: #26303b;
      cursor: pointer;
    }
  }
}
</style>
