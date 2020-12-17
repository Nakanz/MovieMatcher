<template>
  <q-page class="flex flex-center">
    <q-card dark
      bordered>
      <img
        alt="MovieMatcher"
        src="~assets/MMHeader2.png"
      >
      <br>
      <q-btn
        class="full-width"
        color="primary"
        label="Enter"
        glossy
      @click="loginDialog = true"/>
      <q-dialog
        v-model="loginDialog"
        full-width
        full-height
      >
        <q-card style="width: 300px">
          <q-card-section>
            <div class="text-h6">Login</div>
          </q-card-section>

          <q-card-section class="q-pt-none">
            enter your username and password.
          </q-card-section>
          <q-card-section class="login-form">
            <q-input standout="bg-teal text-white" v-model="text" label="Username" />
            <q-input standout="bg-teal text-white" v-model="text" label="Password" />
          </q-card-section>
          <q-card-actions align="right" class="bg-white text-teal">
            <q-btn flat label="OK" v-close-popup />
          </q-card-actions>
        </q-card>
      </q-dialog>
    </q-card>
  </q-page>
</template>

<script>
export default {
    data () {
      return {
          loginDialog: false
      }
    }
}
</script>
