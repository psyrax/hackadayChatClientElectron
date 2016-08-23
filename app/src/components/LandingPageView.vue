<style scoped>
  img {
    margin-top: -25px;
    width: 450px;
  }
</style>

<template>
  <div>
    <img src="LandingPageView/assets/logo.png" alt="electron-vue">
    <h1>Welcome.</h1>
    <current-page></current-page>
    <versions></versions>
    <links></links>
    <oauth-login></oauth-login>
  </div>
</template>

<script>
  import CurrentPage from './LandingPageView/CurrentPage'
  import Links from './LandingPageView/Links'
  import Versions from './LandingPageView/Versions'
  import OauthLogin from './LandingPageView/OauthLogin'

  export default {
    components: {
      CurrentPage,
      Links,
      Versions,
      OauthLogin
    },
    name: 'landing-page'
  }
</script>
