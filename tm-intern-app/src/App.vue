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
import 'normalize.css'

export default {
  name: 'home',
  components: {
    Header
  }
}
</script>

<style>
#app{
  margin:0;
  color:#444;
}

Header{
  position: fixed;
  top :0;
}
</style>
