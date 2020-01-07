<template>
  <div class="header">
    <el-header>
      <h1 class="title">ROHSTEIN</h1>
    </el-header>
    <div class="menu">
      <el-button type="success" class="el-icon-user-solid btn" circle></el-button>
      <el-button type="success" class="el-icon-s-tools btn" circle></el-button>
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
@import url('https://fonts.googleapis.com/css?family=Anton&display=swap');

.header{
  height: 100px;
  background: #444;
  color: #fff;
  font-weight: bold;
}

.title{
  font-family: 'Anton', sans-serif;
  letter-spacing: 5px;
  text-align: left;
}

.menu{
  text-align: right;
}

.btn{
  margin:50px 20px;
}

</style>
