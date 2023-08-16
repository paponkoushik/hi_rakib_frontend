<template>
  <div>
    <div v-html="content"></div>
  </div>
</template>

<script>
import axios from "axios";

export default {
  name: "case",
  head() {
    return {
      title: 'Rakib - Case Study'
    }
  },
  data() {
    return {
      content: '',
      backendUrl: 'http://127.0.0.1:8000'
    }
  },
  created() {
    this.getCase()
  },
  methods: {
    async getCase() {
      let caseStudy = await axios.get(this.backendUrl + '/api/case-study/'+ this.$route.params.case)
        .then(({data}) => {
          this.content = data.content
          if (data.content > 0) {
            this.content = data.content
          } else {
            this.content = `<td>No content available<td>`
          }
        }).catch(err => {
          console.log('case error')
        })
    },
  }
}
</script>

<style scoped>

</style>
