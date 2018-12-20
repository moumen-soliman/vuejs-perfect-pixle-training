<template>
  <div id="app">
    <router-view :userInfo="userInfo"/>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      userInfo: {
        name: 'Khalid',
        team: 'Nasaq',
        board: 'UI/UX'
      }
    }
  }
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css?family=Roboto');
@import '../node_modules/bootstrap/scss/bootstrap.scss';
body {
  background: #f5f7fa;
  #app {
    font-family: 'Roboto', sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    font-weight: normal;
    font-style: normal;
    font-stretch: normal;
    line-height: normal;
    letter-spacing: normal;
  }
}
</style>
