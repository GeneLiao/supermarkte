<template>
    <el-menu
                    background-color="#2d3a4f"
                    unique-opened
                    active-text-color="rgb(64, 158, 255)"
                    :default-active="this.$route.path"
                    router
                     > 
                    <!-- 
                         1.设置整体背景颜色
                         2.是否只保持一个子菜单的展开
                         3.激活的字体的颜色
                         4.当前激活菜单的index
                         5.是否使用 vue-router 的模式，启用该模式会在激活导航时以 index 作为 path 进行路由跳转
                     -->
                    <!-- 导航一 -->
                    <el-submenu index="1">
                        <template slot="title"><i class="el-icon-setting"></i>系统管理</template>
                            <el-menu-item index="/">系统信息</el-menu-item>
                    </el-submenu>
                    <!-- 导航二 -->
                    <el-submenu index="2">
                        <template slot="title"><i class="el-icon-menu"></i>账号管理</template>
                            <el-menu-item index="/accountmanage">账号管理</el-menu-item>
                            <el-menu-item index="/accountadd">添加账号</el-menu-item>
                            <el-menu-item index="/passwordmodify">密码修改</el-menu-item>
                    </el-submenu>
                    <!-- 导航三 -->
                    <el-submenu index="3">
                        <template slot="title"><i class="el-icon-goods"></i>商品管理</template>
                            <el-menu-item index="/goodsmanage">商品管理</el-menu-item>
                            <el-menu-item index="/goodsadd">添加商品</el-menu-item>
                    </el-submenu>
                    <!-- 导航四 -->
                    <el-submenu index="4">
                        <template slot="title"><i class="el-icon-date"></i>统计管理</template>
                            <el-menu-item index="/salestatistics">销售统计</el-menu-item>
                    </el-submenu>
            </el-menu>
</template>
<script>

export default {};
</script>
<style lang="less">
.el-menu {
  border: none; //不让每次点击多出一点
  .el-submenu {
    .el-submenu__title {
      //两个杠title
      color: #fff;
    }
  }
  .el-menu-item {
    color: #fff;
  }
}
</style>


