<template>
    <q-page>
        Halaman Login
    <q-form
      @submit="onSubmit"
      @reset="onReset"
      class="q-gutter-md"
    >
      <q-input
        filled
        v-model="name"
        label="Your name"
        lazy-rules
        :rules="[ val => val && val.length > 0 || 'Tolong isi username']"
      />
      <q-input
        filled
        v-model="username"
        label="Your name"
        lazy-rules
        :rules="[ val => val && val.length > 0 || 'Tolong isi username']"
      />

      <q-input
        filled
        type="password"
        v-model="password"
        label="Isikan Password *"
        lazy-rules
        :rules="[
          val => val !== null && val !== '' || 'Tolong Ketik',
        ]"
      />

      <q-input
        filled
        type="password"
        v-model="rpassword"
        label="Isikan Password *"
        lazy-rules
        :rules="[
          val => val !== null && val !== '' || 'Tolong Ketik',
        ]"
      />
      <div>
        <q-btn label="Submit" type="submit" color="primary"/>
        <q-btn label="Reset" type="reset" color="primary" flat class="q-ml-sm" />
      </div>
    </q-form>
    </q-page>
</template>
<script>
export default {
  data () {
    return {
      name: null,
      username: null,
      password: null,
      rpassword: null
    }
  },
  methods: {
    onSubmit () {
      console.log('Ini Fungsi Submit')
    },
    onReset () {
      console.log('ini fungsi reset')
    }
  }
}
</script>
