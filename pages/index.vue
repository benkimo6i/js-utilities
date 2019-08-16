<template>
  <div class="container">
    <div>
      <h1 class="title">
        js-utilities
      </h1>
      <h2 class="subtitle">
        Resource for common utility functions in vanilla js
      </h2>
      <div class="links">
        <utility-link />
      </div>
    </div>
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'
import UtilityLink from '~/components/UtilityLink.vue'

export default {
  components: {
    Logo,
    UtilityLink
  }
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  padding: 50px 30px;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 42px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 25px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
