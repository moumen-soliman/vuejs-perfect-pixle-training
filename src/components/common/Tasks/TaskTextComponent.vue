<template>
  <div>
    <div class="task-text-card">
      <div class="task-text-card--content">
        <div class="task-text-card--content--headline">
          <h6>{{taskText.name}}</h6>
        </div>
        <div class="task-text-card--content--clip">
          <img src="@/assets/icons/svg/clip.svg" class="clip-icon" alt="Nello - clip">
          <span>{{taskText.attachmentNumber}}</span>
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
  name: 'TaskTextComponent',
  props: ['jobsColor'],
  components: {
    TaggedPeople,
  },
  data () {
    return {
      taskText: {
        name: 'Task name',
        attachmentNumber: '3'
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
    padding: 18px 13px;
    &--headline {
      font-size: 12px;
      color: #000;
      font-weight: 500;
    }
    &--clip {
      color: #a9a9a9;
      margin-bottom: 17px;
      img {
        width: 11px;
        height: 11px;
      }
      span {
        font-size: 13px;
      }
    }
  }
}
</style>
