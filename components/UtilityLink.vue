<template>
  <div class="container-flex">
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
          },
          {
            author: 'Ben Kim',
            id: 'url-query-params',
            title: 'URL Query Params'
          }
        ]
      }
    }
  }
</script>

<style>
  .container-flex {
    display: flex;
    flex-wrap: wrap;
  }

  .container-flex .site-link {
    margin-right: 15px;
  }
</style>