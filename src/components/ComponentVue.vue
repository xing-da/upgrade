<template>
  <div>
    <el-container class="box">
      <el-header>practice</el-header>
      <el-container>
        <el-aside width="200px">
          <el-row class="tac">
            <el-col :span="24">
              <el-menu
                default-active="2"
                class="el-menu-vertical-demo"
                @open="handleOpen"
                @close="handleClose"
              >
                <el-submenu index="1">
                  <template slot="title">
                    <i class="el-icon-location"></i>
                    <span>导航一</span>
                  </template>
                  <el-menu-item-group>
                    <el-menu-item index="1-1">选项1</el-menu-item>
                    <el-menu-item index="1-2">选项2</el-menu-item>
                  </el-menu-item-group>
                  <el-menu-item-group>
                    <el-menu-item index="1-3">选项3</el-menu-item>
                  </el-menu-item-group>
                  <el-submenu index="1-4">
                    <template slot="title">选项4</template>
                    <el-menu-item index="1-4-1">选项1</el-menu-item>
                  </el-submenu>
                </el-submenu>

                <el-menu-item index="2">
                  <i class="el-icon-menu"></i>
                  <span slot="title">导航二</span>
                </el-menu-item>

                <el-menu-item index="3">
                  <i class="el-icon-document"></i>
                  <span slot="title">导航三</span>
                </el-menu-item>

                <el-menu-item index="4">
                  <i class="el-icon-setting"></i>
                  <span slot="title">导航四</span>
                </el-menu-item>
                
              </el-menu>
            </el-col>
          </el-row>
        </el-aside>
        <el-main>Main</el-main>
      </el-container>
    </el-container>
  </div>
</template>

<script>
export default {
  name: "PerksComponentVue",

  data() {
    return {};
  },

  mounted() {},

  methods: {
    handleOpen(key, keyPath) {
      console.log(key, keyPath);
    },
    handleClose(key, keyPath) {
      console.log(key, keyPath);
    },
  },
};
</script>

<style lang="less" scoped>
.box {
  width: 100vw;
  height: 100vh;
}

.el-header {
  background-color: #b3c0d1;
  color: #333;
  text-align: center;
  line-height: 60px;
}

.el-aside {
  background-color: #d3dce6;
  color: #333;
  text-align: center;
  line-height: 200px;
}

.el-main {
  background-color: #e9eef3;
  color: #333;
  text-align: center;
  line-height: 160px;
}
</style>
