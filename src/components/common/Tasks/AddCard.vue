<template>
  <div>
    <div class="col add-card">
      <span>Add card</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'AddCard',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
.add-card {
  text-align: center;
  padding: 21px;
  border-radius: 6px;
  box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.1);
  background-color: #ffffff;
  margin: 10px;
  width: 100%;
  span {
    font-size: 14px;
    color: #d7d6d6;
  }
}

@media screen and (max-width: 767px) {
  .add-card {
    margin: 10px 0;
  }
}
</style>
