<template>
  <div>
    <select v-model="selectedCity">
      <option value="">선택</option>
      <option value="02">서울</option>
      <option value="031">경기</option>
      <option value="064">제주</option>
    </select>
  </div>
</template>
<script>
export default {
  components: {},
  data() {
    return {
      selectedCity: ''
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {}
}
</script>
