<template>
  <div class="home">
    <h1>Hi, I'm Ella Nicole Rivera</h1>
    <p class="lead">{{ msg }}</p>
    <div class="alert alert-info mt-4" role="alert">
      <strong>Open to opportunities!</strong> Browse my projects, read my latest notes, or get in touch if you'd like to work together.
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomePage',
  data () {
    return {
      msg: 'Web developer building clean, responsive, and maintainable web applications.'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.home {
  padding: 20px 0;
}
h1 {
  font-weight: 700;
  color: #111123;
}
</style>
