<template>
  <div class="header">
    <p class="title">テクノモバイル 新卒採用Apps</p>
    <div class="menu">
      <p>menu | menu | menu | menu</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Header'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.header{
  color: white;
  font-family: arial black;
  position: absolute;
  left:0;
  top:0;
  width: 100%;
  background:#000;
}

.title{
  text-align: left;
}

.menu{
  text-align: right;
}

</style>
