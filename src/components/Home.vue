<template>
  <el-container class="home">
    <el-header>
      <div class="logo"></div>
      <div class="title">
        <h1>电商后台管理系统</h1>
      </div>
      <div class="logout">
        <span>欢迎光临</span>
        <a href="javascript:;">退出</a>
      </div>
    </el-header>
    <el-container>
      <el-aside width="200px">Aside</el-aside>
      <el-main>Main</el-main>
    </el-container>
  </el-container>
</template>

<script>
export default {

}
</script>

<style lang="less" scoped>
  // lang:设置语言 less sass stylus
  // scoped: 如果设置了，表示样式只会在当前组件生效， 我们的style都应该scoped
  // 如果当前组件添加了scoped属性，  1. 组件中所有的元素都会添加一个随机属性
  //  data-v-xxxxx
  // 2. 我们写的所有的样式的都会自动添加上属性选择器  div [data-v-xxxxx]

  // 我们通过别名@ 配置了绝对路径，在less中无法使用，如果想要用 ~
  .home {
    height: 100%;

    .el-header {
      background-color: #B3C1CD;
      display: flex;

      .logo {
        width: 180px;
        background-image: url('~@/assets/logo.png');
        background-size: contain;
        background-repeat: no-repeat;
        background-position: center center;
      }

      .logout {
        width: 180px;
        line-height: 60px;
        text-align: center;
        font-weight: 700;

        a {
          color: brown;
        }
      }

      .title {
        flex: 1;

        h1 {
          line-height: 60px;
          text-align: center;
          color: #fff;
          font-size: 30px;
        }
      }
    }

    .el-aside {
      background-color: #545c64;
    }

    .el-main {
      background-color: #eaeef1;
    }
  }
</style>
