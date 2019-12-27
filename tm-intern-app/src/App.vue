<template>
  <div id="app">
    <Header/>
    <!-- <SideNav/>を呼び出す予定 -->
    <router-view/>
  </div>
</template>
<script>
// @ is an alias to /src
import Header from '@/components/Header.vue'

export default {
  name: 'home',
  components: {
    Header
  }
}
</script>

<style>
#app{
  color:#444; 
}
</style>
