<template>
  <div>
    <Navbar :userInfo="userInfo" />
    <TeamCard :userInfo="userInfo" />
    <TaskCard :userInfo="userInfo" />
  </div>
</template>

<script>
import Navbar from './common/Navbar';
import TeamCard from './common/TeamCard';
import TaskCard from './common/TaskCard';

export default {
  name: 'Home',
  props: ['userInfo'],
  components: {
    Navbar,
    TeamCard,
    TaskCard
  },
  data () {
    return {
      isHidden: false,
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>

</style>
