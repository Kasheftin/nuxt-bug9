<template>
  <section class="container">
    <div>
      <h1 class="title">
        Main Page
      </h1>
      <div class="links">
        <nuxt-link to="/sub/1" class="button--green">Go to 1</nuxt-link>
        <nuxt-link to="/sub/2" class="button--green">Go to 2</nuxt-link>
      </div>
    </div>
  </section>
</template>

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
