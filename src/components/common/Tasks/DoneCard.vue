<template>
  <div>
    <div class="done-block" :style="{background: `${jobsColor}`}">
      <span>Done</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'DoneCard',
  props: ['jobsColor'],
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
.done-block {
  text-align: center;
  width: 100%;
  border-radius: 6px;
  position: relative;
  padding: 42px;
  span {
    margin: auto;
    color: white;
  }
}
</style>
