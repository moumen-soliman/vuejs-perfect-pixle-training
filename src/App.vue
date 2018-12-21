<template>
  <div id="app">
    <router-view :userInfo="userInfo"/>
    <FlowButton />
  </div>
</template>

<script>
import FlowButton from './components/common/FlowButton';

export default {
  name: 'App',
  components: {
    FlowButton
  },
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
@import url('https://fonts.googleapis.com/css?family=Roboto:300i,400,400i,500,500i,700,700i');
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
    overflow-y: hidden;
    box-sizing: border-box;
  }
}
</style>
