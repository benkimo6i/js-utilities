<template>
  <div>
    <n-link :key="link.id" v-for="link in links" :to="`/utilities/${link.id}`">
      <p>{{ link.title }}</p>
      <p>{{ link.author }}</p>
    </n-link>
  </div>
</template>

<script>
  export default {
    data () {
      return {
        links: [
          {
            author: '/images/a-wright.png',
            id: 'anderson-wright',
            title: 'Anderson Wright'
          }
        ]
      }
    }
  }
</script>

<style lang="scss">

</style>