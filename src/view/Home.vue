<template>
  <div class="container">
    <h1>{{title}}</h1>
    <div class="wrapper">
      <v-form-search />
      <v-about-button/>
    </div>
  </div>
</template>

<script>
import FormSearch from '@/components/FormSearch'
import AboutButton from '@/components/AboutButton'

export default {
  name: 'Home',
  data () {
    return {
      title: 'Janus Plataform'
    }
  },
  components: {
    'v-form-search': FormSearch,
    'v-about-button': AboutButton
  }
}
</script>

<style scoped>
</style>
