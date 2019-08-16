<template>
  <div class="container">
    <div>
      <div class="ice-cream">
        <img class="ice-cream-cone" alt="ice cream cone" src="/ice-cream.png"/>
        <h1 class="title">js-utilities</h1>
      </div>
      <h2 class="subtitle">Resource for common utility functions in vanilla js</h2>
      <div class="links"><utility-link /></div>
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
  max-width: 1200px;
  min-height: 100vh;
  padding: 50px 30px;
}

.title {
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

.ice-cream {
  display: flex;
  margin-bottom: 10px;
}

.ice-cream-cone {
  height: auto;
  margin-right: 15px;
  max-width: 40px;
  width: 100%;
}
</style>
