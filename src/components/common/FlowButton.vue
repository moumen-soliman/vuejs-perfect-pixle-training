<template>
  <div>
    <div class="flow-button">
      <img src="@/assets/icons/svg/invalid-name.svg" />
    </div>
  </div>
</template>

<script>
export default {
  name: 'FlowButton',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss"scoped>
.flow-button {
  width: 79px;
  height: 79px;
  background-color: #7148fc;
  border-radius: 50%;
  position: fixed;
  left: 53px;
  bottom: 64px;
  cursor: pointer;
  &:hover {
    opacity: 0.8;
  }
  img {
    width: 25px;
    position: absolute;
    left: 34%;
    top: 33%;
  }
}


@media screen and (max-width: 767px) {
    .flow-button {
      left: 11px;
      bottom: 11px;
    }
}
</style>
