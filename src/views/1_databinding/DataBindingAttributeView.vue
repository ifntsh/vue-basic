<template>
  <div>
    <input type="text" name="" id="" v-bind:value="userId" readonly>
    <br>
    <input type="text" name="" id="" :value="userId" readonly>
    <br>
    <img :src="imgSrc" alt="" style="width: 100px; height: auto;" />
    <br>
    <input type="search" name="" id="" v-model="txt1">
    <button :disabled="txt1 === ''">조회</button>
  </div>
</template>
<script>
export default {
  components: {},
  data() {
    return {
      userId: 'hipark',
      imgSrc: 'https://avatars.githubusercontent.com/u/6128107?s=280&v=4',
      txt1: ''
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {}
}
</script>
