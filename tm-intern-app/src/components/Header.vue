<template>
  <div>
    <el-header class="header" height="90px">
      <h1 class="title">ROHSTEIN</h1>
      <div class="menu">
        <el-button type="success" class="el-icon-user-solid btn" circle></el-button>
        <el-button type="success" class="el-icon-s-tools btn" circle></el-button>
      </div>
    </el-header>
    <!-- <slide>
      <a id="home" href="#">
        <span>Home</span>
      </a>
      <a id="about" href="#">
        <span>About</span>
      </a>
      <a id="contact" href="#">
        <span>Contact</span>
      </a>
    </slide> -->
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
  width:100%;
  background: #444;
  color: #fff;
  font-weight: bold;
}

.title{
  font-family: 'Anton', sans-serif;
  letter-spacing: 5px;
  text-align: left;
  margin:0;
}

.menu{
  text-align: right;
}

.btn{
  margin: 0;
}

.sideBtn{
  
}

.sideNav{
  position:fixed;
  margin:0;
  z-index:10;
}

</style>
