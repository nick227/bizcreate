<template>
<q-page  class="docs-input row justify-center">
        <div class="col-xl-4 col-lg-6 col-md-6 col-sm-12 col-xs-12 q-pa-xl dark">
          <div class="text-center">
            <p class="q-display-1 text-weight-bolder q-pt-lg">BizCreate</p>
            <p class="q-title text-weight-bold q-ma-none">Social Login</p>
          </div>
          <div class="q-mt-xl">
            <q-btn
              color="primary" glossy push class="full-width"
              icon="fab fa-facebook-f" label="Login with Facebook"
              size="md" @click="auth('facebook')" >
            </q-btn>
          </div>
       </div>
    </q-page>
</template>
<script>
export default {
  meta () {
    return {}
  },
  name: 'LoginPage',
  components: {},
  data () {
    return {}
  },
  methods: {
    auth (network) {
      this.$hello(network).login()
        .then((res) => {
          this.$router.push('profile')
        })
    }
  },
  mounted () {}
}
</script>
