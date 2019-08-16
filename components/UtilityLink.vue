<template>
  <div>
    <n-link class="site-link" :key="link.id" v-for="link in links" :to="`/utilities/${link.id}`">
      <h3>{{ link.title }}</h3>
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
            author: 'John Moore',
            id: 'get-cookies',
            title: 'Get Cookies'
          }
        ]
      }
    }
  }
</script>

<style lang="scss">

</style>