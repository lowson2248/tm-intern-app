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
  color:#444;
  margin-top:100px;
}

Header{
  position: fixed;
  top:0;
  z-index:10;
}

</style>
