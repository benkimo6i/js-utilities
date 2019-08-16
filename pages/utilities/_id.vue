<template>
  <div class="utility-content">
    <p class="utility-author"><span>Author</span> {{ post.author }}</p>
    <h1 class="utility-title">{{ post.title }}</h1>
    <p class="utility-desc">{{ post.description }}</p>
    <div class="utility-code">{{ post.code }}</div>
  </div> 
</template>

<script>
  export default {
    data () {
      return {
        id : this.$route.params.id,
        utilities: [
          {
            author: 'Anderson Wright',
            description: 'Close your eyes and just do it.',
            id: 'anderson-wright',
            title: 'Nike: “Run It”',
            code: '158511959'
          }
        ]
      }
    },
    computed: {
      post () {
        return this.utilities.find(utility => utility.id === this.id);
      }
    }
  }
</script>

<style lang="scss">

</style>