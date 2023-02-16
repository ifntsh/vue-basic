<template>
  <div>
    <h1>Hello {{ userName }}</h1>
    <p>{{ message }}</p>
  </div>

</template>
<script>
export default {
  data() {
    return {
      userName: 'Hi Park',
      message: 'Welcome 웰컴 메시지',
      arr: [],
      obj: {}
    }
  }
}
</script>
<style scoped>
.text-red {
  color: red;
}
</style>
