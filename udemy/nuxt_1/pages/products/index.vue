<template>
  <div>
    <h1>the products</h1>

    <div>
      <input type="text" v-model="pid">
      <button @click="onLoadPid">load pid</button>
    </div>

    <button @click="$router.push('/products/2')">Products2</button>
    <nuxt-link to="/products/1">Products1</nuxt-link>
  </div>
</template>

<script>
export default {
  data() {
    return {
      pid: ''
    }
  },
  methods: {
    onLoadPid() {
      this.$router.push('/products/' + this.pid);
    }
  }
}
</script>
