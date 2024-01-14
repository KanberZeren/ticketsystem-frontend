<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
  </div>
</template>

<script>
export default {
  name: 'HomePage',
  props: {
    msg: String
  }
}
</script>

<style scoped>
h1{
  margin-left: 20px;
  flex-direction: column;
  padding: 20px;
}
</style>
