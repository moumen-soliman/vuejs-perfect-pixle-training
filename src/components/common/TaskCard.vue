<template>
  <div class="row">
    <div class="col-sm-12 col-md-6 col-lg-4 col-xl-3" v-for="job in jobs" :key="job.id">
      <div class="task-card col">
        <div class="task-card--content">
          <div class="task-card--content--headline">
            <div class="circle" :style="{borderColor: `${job.color}`}"></div>
            <h3 :style="{color: `${job.color}`}">{{job.headline}} area</h3>
          </div>
          <div v-if="job.tasks.includes('text')">
            <TaskTextComponent class="item" :jobsColor="job.color" />
          </div>
          <div v-if="job.tasks.includes('done')">
            <DoneCard class="item" :jobsColor="job.color" />
          </div>
          <div v-if="job.tasks.includes('one')">
            <TaskOneComponent class="item" />
          </div>
          <div v-if="job.tasks.includes('multiplie')">
            <TaskMultiplieComponents :jobsColor="jobsColor"/>
          </div>
        </div>
      </div>
      <AddCard />
    </div>
  </div>
</template>

<script>
import TaskTextComponent from './Tasks/TaskTextComponent';
import DoneCard from './Tasks/DoneCard';
import TaskOneComponent from './Tasks/TaskOneComponent';
import TaskMultiplieComponents from './Tasks/TaskMultiplieComponents';
import AddCard from './Tasks/AddCard';

export default {
  name: 'TaskCard',
  props: ['userInfo'],
  components: {
    TaskTextComponent,
    DoneCard,
    TaskOneComponent,
    TaskMultiplieComponents,
    AddCard
  },
  data () {
    return {
      jobs: [
        {
          id: 1,
          headline: 'Design',
          tasks: ['multiplie', 'text'],
          color: '#7148fc'
        },
        {
          id: 2,
          headline: 'Frontend',
          tasks: ['text', 'done', 'one'],
          color: '#f5a623'
        },
        {
          id: 3,
          headline: 'Development',
          tasks: ['one', 'multiplie'],
          color: '#4a90e2'
        },
        {
          id: 4,
          headline: 'Board',
          tasks: ['text', 'done', 'one'],
          color: '#04cda0'
        }
      ],
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
    height: fit-content;
    &--content {
      padding: 44px 28px 20px 28px;
      .item {
        margin-bottom: 9px;
      }
      &--headline {
        padding-bottom: 36px;
        .circle {
          width: 7px;
          height: 7px;
          border-radius: 50%;
          border-width: 1px;
          border-style: solid;
          display: inline-block;
        }
        h3 {
          font-size: 22px;
          font-weight: 400;
          color: #7148fc;
          padding-left: 7px;
          display: inline-block;
          font-weight: 500;
        }
      }
    }
  }
}
@media screen and (max-width: 767px){
    .row {
      margin: 0;
      .task-card {
        margin: 0;
      }
    }
}
</style>
