<template>
  <div>
    <select name="" id="" @change="changeCity($event)" v-model="selectedCity">
      <option value="">==도시선택==</option>
      <option :value="city.cityCode" :key="city.cityCode" v-for="city in cityList">{{ city.title }}</option>
    </select>

    <select name="" id="">
      <option value="">==동선택==</option>
      <option :value="dong.dongCodeg" :key="dong.dongCode" v-for="dong in selectedDongList">{{ dong.dongTitle }}
      </option>
    </select>

    <!-- @change="changeCity" 을 빼고 사용하려면 가능하지만 가독성 떨어짐 -->
    <!-- <select name="" id="">
      <option value="">==동선택==</option>
      <option :value="dong.dongCodeg" :key="dong.dongCode"
        v-for="dong in dongList.filter((dong) => dong.cityCode === selectedCity)">{{ dong.dongTitle }}
      </option>
    </select> -->

  </div>
</template>
<script>
export default {
  components: {},
  data() {
    return {
      selectedCity: '',
      cityList: [
        { cityCode: '02', title: '서울' },
        { cityCode: '031', title: '경기' },
        { cityCode: '064', title: '제주' }
      ],
      dongList: [
        { cityCode: '02', dongCode: '1', dongTitle: '서울 1동' },
        { cityCode: '02', dongCode: '2', dongTitle: '서울 2동' },
        { cityCode: '02', dongCode: '3', dongTitle: '서울 3동' },
        { cityCode: '02', dongCode: '4', dongTitle: '서울 4동' },
        { cityCode: '031', dongCode: '1', dongTitle: '경기 1동' },
        { cityCode: '031', dongCode: '2', dongTitle: '경기 2동' },
        { cityCode: '031', dongCode: '3', dongTitle: '경기 3동' },
        { cityCode: '064', dongCode: '1', dongTitle: '제주 1동' },
        { cityCode: '064', dongCode: '2', dongTitle: '제주 2동' }
      ],
      selectedDongList: []
    }
  },
  setup() { },
  created() { },
  mounted() { },
  unmounted() { },
  methods: {
    changeCity(event) {
      console.log(event.target.tagName)
      this.selectedDongList = this.dongList.filter(dong => dong.cityCode === this.selectedCity)
    }
  }
}
</script>
