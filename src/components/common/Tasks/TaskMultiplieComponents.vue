<template>
  <div>

  </div>
</template>

<script>
export default {
  name: 'TaskCard',
  props: ['userInfo'],
  data () {
    return {
      tasks: [
        {
          name: 'Task name',
          image: 'https://upload.wikimedia.org/wikipedia/commons/thumb/2/21/Solid_black.svg/2000px-Solid_black.svg.png',
          videoThumbail: 'https://upload.wikimedia.org/wikipedia/commons/thumb/2/21/Solid_black.svg/2000px-Solid_black.svg.png',
          text: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry\'s standard dummy text ever since the 1500s'
        }
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>

</style>
