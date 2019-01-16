<template>
  <section class="container">
    <div>
      <h1 class="title">
        {{ route.path }}
      </h1>
      <div class="links">
        <nuxt-link to="/" class="button--green">Go to Main Page</nuxt-link>
        <a class="button--green" @click="goto(1)">Go to 1</a>
        <a class="button--green" @click="goto(2)">Go to 2</a>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  computed: {
    route () { return this.$route }
  },
  fetch () {
    return new Promise((resolve, reject) => {
      setTimeout(() => {
        resolve()
      }, 1000)
    })
  },
  methods: {
    goto (n) {
      this.$router.push({path: '/sub/' + n})
      setTimeout(() => {
        this.$router.push({query: {p1: 'v2'}})
      }, 500)
    }
  }
}
</script>

<style>

.container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.links {
  padding-top: 15px;
}
</style>
