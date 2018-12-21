<template>
  <div>
    <div class="tagged-people row">
      <div class="col col-sm">
        <div class="float-left">
          <div class="tagged-people--add">
            <span>+</span>
          </div>
          <div class="tagged-people--employ">
            <img src="@/assets/icons/jpg/test.jpg" />
            <img src="@/assets/icons/jpg/test.jpg" />
            <img src="@/assets/icons/jpg/test.jpg" />
          </div>
          <div class="tagged-people--overflow" :style="{background: `${jobsColor}`}">
            <span>+4</span>
          </div>
        </div>
      </div>
      <div class="col col-sm">
        <div class="float-right">
          <div class="tagged-people--line"></div>
          <div class="tagged-people--line"></div>
          <div class="tagged-people--line"></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TaggedPeople',
  props: ['jobsColor'],
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
.tagged-people {
  &--add {
    display: inline-block;
    background: #f9f8fc;
    width: 21px;
    height: 21px;
    border-radius: 50%;
    text-align: center;
    position: relative;
    span {
      font-size: 14px;
      color: #a9a9a9;
      margin: auto;
      font-weight: 500;
      position: static;
      padding: 0px 7px;
    }
  }
  &--employ {
    display: inline-block;
    img {
      border-radius: 50%;
      width: 18px;
      margin-left: -13px;
      &:first-child {
        margin-left: -6px;
      }
    }
  }
  &--overflow {
    margin-left: -11px;
    display: inline-block;
    width: 21px;
    height: 21px;
    border-radius: 50%;
    text-align: center;
    position: relative;
    span {
      color: white;
      font-size: 12px;
      margin-right: 1px;
    }
  }
  &--line {
    display: inline-block;
    width: 19px;
    height: 2px;
    border-radius: 1px;
    background-color: #7148fc;
    &:nth-child(2) {
      opacity: 0.59;
    }
    &:last-child {
      opacity: 0.25;
    }
  }
}
</style>
