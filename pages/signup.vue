<template>
  <v-layout justify-center>
    <v-flex xs12 sm6>
      <div class="logo-wrapper">
        <nuxt-link to="/">
          <logo font-size="56px"/>
        </nuxt-link>
      </div>
      <v-card class="px-3 pt-3">
        <v-card-title class="headline pb-0">Sign Up</v-card-title>
        <v-card-text>
          <v-text-field v-model="email" type="email" label="이메일" :rules="[emailRule]"/>
          <v-text-field v-model="password" type="password" label="비밀번호" :rules="[passwordRule]"/>
          <v-text-field
            v-model="passwordConfirm"
            type="password"
            label="비밀번호 확인"
            :rules="[passwordConfirmRule]"
          />
          <br>
          <span>In order to protect your account, make sure your password:</span>
          <ul class="list">
            <li>Is longer than 7 characters</li>
            <li>Does not match or significantly contain your username, e.g. do not use 'username123'.</li>
          </ul>
          <v-checkbox
            v-model="eula"
            class="checkbox ma-0"
            color="primary"
            label="이용약관 동의"
            hide-details
          />
          <v-checkbox
            v-model="privacy"
            class="checkbox ma-0"
            color="primary"
            label="개인정보 취급방침 동의"
            hide-details
          />
          <br>
          <v-btn block color="primary" :disabled="!eula || !privacy" flat>Create New Accout</v-btn>
          <v-btn block flat href="/login">or, Login</v-btn>
        </v-card-text>
      </v-card>
    </v-flex>
  </v-layout>
</template>

<script>
import Logo from '@/components/Logo'

const EMAIL_REGEX = /^(([^<>()\[\]\\.,;:\s@"]+(\.[^<>()\[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/

export default {
  layout: 'empty',
  components: {
    Logo
  },
  data() {
    return {
      email: '',
      password: '',
      passwordConfirm: '',
      eula: false,
      privacy: false
    }
  },
  methods: {
    emailRule(text) {
      const { email } = this
      if (email && !EMAIL_REGEX.test(email)) {
        return '이메일 형식이 올바르지 않습니다'
      }
      return true
    },
    passwordRule(text) {
      const { password } = this
      if (password.length < 7) {
        return '비밀번호는 7글자 이상이어야 합니다.'
      }
      return true
    },
    passwordConfirmRule(text) {
      const { password, passwordConfirm } = this
      if (password && passwordConfirm && password !== passwordConfirm) {
        return '비밀번호가 동일하지 않습니다.'
      }
      return true
    }
  }
}
</script>

<style scoped>
.logo-wrapper {
  margin: 0 auto;
  padding: 64px 0 32px;
  text-align: center;
}

.list {
  padding: 8px 16px;
  list-style-type: none;
}

.list li::before {
  content: '\2022';
  color: #212121;
  font-weight: bold;
  display: inline-block;
  width: 16px;
  margin-left: -16px;
}
</style>

<style>
.checkbox .v-input__slot .v-label {
  color: black !important;
}
</style>
