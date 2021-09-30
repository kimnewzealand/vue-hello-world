<template>
  <div id="app">
    <NavBar />
    <TranslateForm />
  </div>
</template>

<script>
import TranslateForm from './components/TranslateForm.vue'
import NavBar from './components/NavBar'

export default {
  name: 'App',
  components: {
    TranslateForm,
    NavBar
  }
}
</script>


