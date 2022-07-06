<template>
  <div id="app">
    <DcHeader />
    <main>
      <DcMain />
    </main>

<!-- 
    <main></main>

    <footer></footer> -->

    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  </div>
</template>

<script>
import DcHeader from './components/DcHeader.vue'
import DcMain from './components/DcMain.vue'


export default {
  name: 'App',
  components: {
    DcHeader,
    DcMain
  }
}
</script>

<style lang="scss">
@import './style/common.scss';
</style>
