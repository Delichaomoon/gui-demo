<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
  <div class="home">
    <Form v-slot="{ errors, values, validate }" @submit="onSubmit">{{ errors }} {{ values }}
    <div class="mb-3">
      <label for="email" class="form-label">Email</label>
      <Field id="email" name="email" type="email" class="form-control" :class="{ 'is-invalid': errors['email'] }"
      placeholder="請輸入 Email" rules="email|required" v-model="user.email"></Field>
      <error-message name="email" class="invalid-feedback"></error-message>
    </div>
    <button class="btn me-2 btn-outline-primary" type="button" @click="validate">驗證</button>
    <button class="btn btn-primary" type="submit">Submit</button>
    </Form>
  </div>
</template>

<script>
/* eslint-disable */
import HelloWorld from '@/components/HelloWorld.vue'
import { Script } from 'vm';

export default {
  name: 'HomeView',
  components: {
    HelloWorld
  },
  data() {
    return {
      user: {},
    };
  },
  methods: {
    onSubmit() {
      console.log(this.user);
    },
  },
  created() {
    console.log(this);
  },
}
</script>