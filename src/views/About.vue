<template>
  <div class="about">
    <h1>This is an about page</h1>
    <button @click="goBack">Back</button>
  </div>
</template>
<script>
// import Name from './components/Name.vue'

export default {
  computed: {
    username() {
      // We will see what `params` is shortly
      return this.$route.params.username
    }
  },
  methods: {
    goBack() {
      window.history.length > 1 ? this.$router.go(-1) : this.$router.push('/')
    }
  }
}
</script>
