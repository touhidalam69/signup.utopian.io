<template>
  <div class="Box__container">
    <div class="Box__inner">     
      <div class="Success">
        <h1>Thanks for confirming your phone number!</h1>
        <p>You’re a few steps away from getting to the top of the list. Check your email and click the email validation link.</p>
        <p>After validating your sign up request with us we’ll look it over for approval. As soon as your turn is up and you’re approved, you’ll be sent a link to finalize your account!</p>
        <div style="height:24px;widht:100%;"><p class="text__error" v-show="this.input_error">{{input_error}}</p></div>
      </div>
    </div>
  </div>
</template>

<script>
import { mapGetters } from 'vuex'
export default {
  computed: {
    ...mapGetters([
    ])
  },
  watch: {
    input_account: function() {
      this.getAccount()
    },
  },
  data() {
    return {
      input_country_code: '',
      input_phone_number: '',
      input_error: ''
    }
  },
  methods: {
    sendPhone() {
      this.$router.push('/confirm_phone')
    }
  }
}
</script>

<style>

.Box__key {
  height: 55.44px;
  width: 336px;
  border-left: 1px solid #E0E2E5;
}

.Success {
    height: 212px;
}

</style>
