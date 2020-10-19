<script>
export default {
  props: [],
  data: () => ({
    error: false,
  }),
  mounted() { },
  methods: { },
};
</script>

<template>
  <div class="recaptcha-widget">
    <div class="recaptcha-widget__alert" v-if="error" @click="reset()">
      Во время проверки Google reCAPTCHA произошла ошибка или время ожидания истекло.
    </div>
    <div class="notation">
      Защита от спама
      <a href="https://www.google.com/recaptcha" target="_blank" rel="nofollow">
        reCAPTCHA
      </a> <i>·</i>
      <a rel="nofollow" href="https://www.google.com/intl/ru/policies/privacy/" target="_blank" class="notation__link">
        Конфиденциальность
      </a> <i>·</i>
      <a rel="nofollow" href="https://www.google.com/intl/ru/policies/terms/" target="_blank" class="notation__link">
        Условия использования
      </a>
    </div>
  </div>
</template>

<style lang="less">
.grecaptcha-badge { visibility: hidden; }

.recaptcha-widget {
  &__alert {
    background-color: #ffb6c1;
  }

  .g-recaptcha {
    display: none;
  }
  .notation {
    text-align: center;
    margin: 10px auto;
    margin-top: 15px;
    max-width: 750px;
    color: #666666;
    font-size: 10px;

    &__link {
      font-size: 10px;
      color: #666666;
      cursor: pointer;
      text-decoration: none;
    }
  }
}
</style>
