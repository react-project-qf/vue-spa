<template>
  <div>
    <p>{{ message.detail }}</p>
  </div>
</template>

<script>
  import { mapState } from 'vuex'

  export default {
    data() {
      return {
        title: 'ERROR!'
      }
    },
    computed: mapState([
      'message'
    ]),
    mounted() {
      console.log(mapState)
      this.$store.commit('SET_MESSAGE', '404 Not Found！')
    },
    components: {}
  }
</script>