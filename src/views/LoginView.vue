<script setup lang="ts">

</script>

<template>
<div class="d-flex justify-center align-center h-screen" >
 <v-card class="pa-8" width="40vw" title="Login">
      <v-form
        v-model="form"
        @submit.prevent="onSubmit"
      >
        <v-text-field
          v-model="email"
          :readonly="loading"
          :rules="[required, checkEmailFormat]"
          class="mb-2"
          clearable
          label="Email"
        ></v-text-field>

        <v-text-field
          v-model="password"
          :readonly="loading"
          :rules="[required]"
          clearable
          label="Password"
          type="password"
          placeholder="Enter your password"
        ></v-text-field>

        <br>

        <v-btn
          :disabled="!form"
          :loading="loading"
          block
          color="success"
          size="large"
          type="submit"
          variant="elevated"
        >
          Sign In
        </v-btn>
      </v-form>
    </v-card>
  </div>
</template>

<script lang="ts">
 export default {
    data: () => ({
      form: false,
      email: null,
      password: null,
      loading: false,
    }),

    methods: {
      onSubmit () {
        if (!this.form) return

        this.loading = true

        setTimeout(() => (this.loading = false), 2000)
      },
      required (v: string) {
        return !!v || 'Field is required'
      },
      checkEmailFormat (v: string) {
        const emailRegex = /^[a-zA-Z0-9.]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$/;
        return emailRegex.test(v) || "Email format incorrect";
      },
    },
  }
</script>