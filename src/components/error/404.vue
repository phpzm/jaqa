<template>
  <div class="error-page window-height window-width bg-light column items-center">
    <div class="error-code bg-primary flex items-center justify-center">
      404
    </div>
    <div>
      <div class="error-card card bg-white column items-center justify-center">
        <i class="text-grey-5">error_outline</i>
        <p class="caption text-center">Oops. Nothing here...</p>
        <p class="text-center group">
          <button v-if="canGoBack" class="button grey small" @click="goBack">
            <i class="on-left">keyboard_arrow_left</i>
            Go back
          </button>
          <router-link to="/">
            <button class="button grey small">
              Go home
              <i class="on-right">home</i>
            </button>
          </router-link>
        </p>
      </div>
    </div>
  </div>
</template>

<script type="text/javascript">
  export default {
    data () {
      return {
        canGoBack: window.history.length > 1
      }
    },
    methods: {
      goBack () {
        window.history.go(-1)
      }
    }
  };
</script>

<style lang="stylus" rel="stylesheet/stylus">
  .error-page
    .error-code
      height: 50vh
      width: 100%
      padding-top: 0
      font-size: 30vmax
      color: rgba(255, 255, 255, .2)
      overflow: hidden
    .error-card
      margin-top: -25px
      width: 90vw
      max-width: 600px
      padding: 50px 10px
      i
        font-size: 5rem
</style>
