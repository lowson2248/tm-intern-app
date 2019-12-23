<template>
  <div class="header">
    <el-header>
      <p class="title">テクノモバイル 新卒採用Apps</p>
      <div class="menu">
        <el-button type="primary" class="el-icon-user-solid icon"></el-button>
        <el-button type="primary" class="el-icon-s-tools icon"></el-button>
      </div>
    </el-header>
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
  font-family:"PingFang SC";
  font-weight: bold;
}

.title{
  text-align: left;
}

.menu{
  text-align: right;
}

i{

}

</style>
