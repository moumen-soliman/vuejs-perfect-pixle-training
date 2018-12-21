<template>
  <div>
    <div class="task-one-card">
      <div class="task-one-card--content">
        <div class="task-one-card--content--headline">
          <h6>{{taskText.name}}</h6>
        </div>
        <div class="task-one-card--content--clip">
          <img src="@/assets/icons/svg/clip.svg" class="clip-icon" alt="Nello - clip">
          <span>{{taskText.attachmentNumber}}</span>
        </div>
        <div class="task-one-card--content--image">
          <img src="@/assets/icons/png/black.png"/>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TaskOneComponent',
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
.task-one-card {
  border: 1px solid #e8e8e8;
  border-radius: 6px;
  margin-bottom: 9px;
  &--content {
    &--headline {
      padding: 18px 0px 0 13px;
      font-size: 12px;
      color: #000;
      font-weight: 500;
    }
    &--clip {
      margin-left: 13px;
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
    &--image {
      img {
        width: 100%;
        height: 114px;
        border-radius: 6px;
        border-top-right-radius: 0;
        border-top-left-radius: 0;
      }
    }
  }
}
</style>
