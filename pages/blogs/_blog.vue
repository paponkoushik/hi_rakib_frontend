<template>
  <div>
    <div v-html="content"></div>
  </div>
</template>

<script>
import axios from "axios";

export default {
  name: "blog",
  head() {
    return {
      title: 'Rakib - Blog'
    }
  },
  data() {
    return {
      content: '',
      backendUrl: 'http://127.0.0.1:8000'
    }
  },
  created() {
    console.log(this.$route.params.blog)
    this.getBlog()
  },
  methods: {
    async getBlog() {
      let blogs = await axios.get(this.backendUrl + '/api/blog/'+ this.$route.params.blog)
        .then(({data}) => {
          if (data.content > 0) {
            this.content = data.content
          } else {
            this.content = `<td>No content available<td>`
          }
        }).catch(err => {
          console.log('blogs error')
        })
    },
  }
}
</script>

<style scoped>

</style>
