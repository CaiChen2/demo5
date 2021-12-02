<template>
    <el-container class="home-container">
      <!-- 侧边栏 -->
      <el-aside width="200px">
        <div>
        <img src="../assets/logo.png" alt="" style="width:50px;height:50px">
        <span>南京理工大学</span>
        </div>
        <!-- 侧边栏 -->
        <el-menu
          background-color="#612994"
          text-color="#fff"
          active-text-color="#ffd04b">
          <!-- 一级菜单 -->
          <el-submenu index="1">
            <template slot="title">
            <i class="el-icon-location"></i>
            <span>导航一</span>
            <!-- 二级菜单 -->
            </template>
              <el-menu-item index="1-1">选项1</el-menu-item>
              <el-menu-item index="1-2">选项2</el-menu-item>
              <el-menu-item index="1-3">选项3</el-menu-item>
          </el-submenu>
        </el-menu>
      </el-aside>
      <el-container>
        <!-- 头部 -->
        <el-header>Header
          <el-button type="info" @click="logout">退出</el-button>
        </el-header>
        <!-- 主体 -->
        <el-main>Main</el-main>
      </el-container>
    </el-container>
</template>

<script>
export default {
  methods: {
    logout () {
      window.sessionStorage.clear()
      this.$router.push('/login')
    }
  }
}
</script>

<style lang="less" scoped>
.home-container{
  height: 100%;
}
.el-header{
  background-color: #612994;
  display: flex;
  justify-content: space-between;
  padding-left: 0;
  align-items: center;
}
.el-aside{
  background-color: #612994;
  color: #fff;
  font-size: 20px;
  align-items: center;
  > div{
    display: flex;
    align-items: center;
    span {
      margin-left: 15px;
    }
  }
}
.el-main{
  background-color: #c4c4c4;
}

</style>
