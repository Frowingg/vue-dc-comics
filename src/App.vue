<template>
  <div id="app">
    <DcHeader />

<!-- 
    <main></main>

    <footer></footer> -->

    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  </div>
</template>

<script>
import DcHeader from './components/DcHeader.vue'

export default {
  name: 'App',
  components: {
    DcHeader
  }
}
</script>

<style>
@import './style/common.scss';
</style>
