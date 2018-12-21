<template>
  <div>
    <div class="task-text-card">
      <div class="task-text-card--content">
        <div class="task-text-card--content--headline">
          <h6>{{taskText.name}}</h6>
        </div>
        <div class="task-text-card--content--paragraph row">
          <div class="col">
            <p>{{taskText.paragraph}}</p>
          </div>
          <div class="col">
            <img src="@/assets/icons/png/black.png" />
          </div>
          <div class="col-12 task-text-card--content--video">
            <img src="@/assets/icons/svg/group-12.svg" class="play-button">
            <img src="@/assets/icons/png/black.png" class="video">
          </div>
        </div>
        <div>
          <TaggedPeople :jobsColor="jobsColor" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import TaggedPeople from './TaggedPeople';

export default {
  name: 'TaskMultiplieComponents',
  props: ['jobsColor'],
  components: {
    TaggedPeople,
  },
  data () {
    return {
      taskText: {
        name: 'Task name',
        paragraph: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry\'s standard dummy text ever since the 1500s'
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
.task-text-card {
  border: 1px solid #e8e8e8;
  border-radius: 6px;
  &--content {
    padding: 30px 10px 16px 10px;
    &--headline {
      font-size: 18px;
      font-weight: 500;
      color: #000;
      margin-bottom: 14px;
    }
    &--paragraph {
      p {
        font-size: 0.5em;
        line-height: 13px;
        color: #292754;
        margin-top: 7px;
      }
      .col {
        img {
          width: 117px;
          height: 81px;
          border-radius: 8px;
          float: right;
        }
      }
    }
      &--video {
        padding-top: 8px;
        padding-bottom: 14px;
        width: 100%;
        img.play-button {
          position: absolute;
          width: 46px;
          height: 46px;
          left: 41%;
          top: 29%;
        }
        img {
          width: 100%;
          height: 109px;
          border-radius: 8px;
          background-color: #000000;
        }
      }
  }
}
</style>
