<template>
  <div class="home">
    Hello world
  </div>
</template>

<script>
import axios from 'axios'
const url = 'https://api.covid19api.com/summary'

export default {
  name: 'Home',
  components: {},
  methods: {
    async fetchCovidData() {
      const {data} = await axios.get(url)
      return data
    }
  },
  async created() {
    const data = await this.fetchCovidData()
    console.log(data)
  }
}
</script>
