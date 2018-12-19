<template>
  <div id="app">
    <div class="main-container">
      <router-view/>
    </div>
  </div>
</template>

<script>
export default {
  name: 'App'
};
</script>

<style lang="scss">
//base file contain variables, website skeleton
@import './assets/style/_base.scss';

#app {
  font-family: $font-family;
}
</style>
