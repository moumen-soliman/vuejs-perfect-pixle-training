<template>
  <div>
    <section class="intro-home-section">
      <div class="container">
        <Navbar></Navbar>
        <div class="intro-home-section-content">


        </div>
      </div>
    </section>
  </div>
</template>

<script>
import Navbar from './Navbar';

export default {
  name: 'Home',
  components: {
    Navbar
  },
  data() {
    return {
      msg: 'عربي جديد',
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit SASS to this component only -->
<style lang="scss">
  section {
    background: url(../assets/images/home/png-icons/screen-shot-2017-12-27-at-8-44-39-am.png), radial-gradient(circle at 50% 51%, #700240, #330219) no-repeat center center;
    -webkit-background-size: cover;
    -moz-background-size: cover;
    -o-background-size: cover;
    background-size: cover;
    height: 100vh;
  }
</style>
