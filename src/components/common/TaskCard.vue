<template>
  <div class="row">
    <div class="task-card col">
      <div class="task-card--content">
        <div class="task-card--content--headline">
          <div class="circle"></div>
          <h3>{{jobs.design}} area</h3>
        </div>

      </div>
    </div>
    <div class="task-card col">
      <div class="task-card--content">
        <div class="task-card--content--headline">
          <div class="circle"></div>
          <h3>{{jobs.design}} area</h3>
        </div>
      </div>
    </div>
    <div class="task-card col">
      <div class="task-card--content">
        <div class="task-card--content--headline">
          <div class="circle"></div>
          <h3>{{jobs.design}} area</h3>
        </div>
      </div>
    </div>
    <div class="task-card col">
      <div class="task-card--content">
        <div class="task-card--content--headline">
          <div class="circle"></div>
          <h3>{{jobs.design}} area</h3>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TaskCard',
  props: ['userInfo'],
  data () {
    return {
      jobs: {
        design: 'Design',
        frontend: 'Frontend',
        development: 'Development',
        board: 'Board'
      },
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
.row {
  margin-right: 35px;
  margin-left: 35px;
    overflow-y: hidden;
  .task-card {
    background: white;
    border-radius: 6px;
    padding: 0;
    box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.1);
    margin: 10px;
    &--content {
      padding: 44px 28px 20px 28px;
      &--headline {
        margin-bottom: 36px;
        .circle {
          width: 7px;
          height: 7px;
          border-radius: 50%;
          border: 1px solid #7148fc;
          display: inline-block;
        }
        h3 {
          font-size: 18px;
          font-weight: 600;
          color: #7148fc;
          padding-left: 7px;
          display: inline-block;
        }
      }
    }
  }
}
</style>
