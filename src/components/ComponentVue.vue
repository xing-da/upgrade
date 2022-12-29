<template>
  <div>
    <el-container class="box">
      <el-header class="header">practice</el-header>
      <el-container>
        <el-aside width="200px">
          <el-row>
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
                    <el-menu-item index="1-1">
                      <router-link to="/q">Q</router-link>
                    </el-menu-item>
                    <el-menu-item index="1-2"
                      ><router-link to="/w">W</router-link></el-menu-item
                    >
                  </el-menu-item-group>
                  <el-menu-item-group>
                    <el-menu-item index="1-3">
                      <nav>
                        <router-link to="/about">About</router-link>
                      </nav>
                    </el-menu-item>
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
        <el-main class="main">
          <router-view />
        </el-main>
      </el-container>
    </el-container>
  </div>
</template>

<script>
import QTestView from "@/views/q/QTestView.vue";
export default {
  components: { QTestView },
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
  .el-header {
    background-image: linear-gradient(120deg, #84fab0 0%, #8fd3f4 100%);
    font-family: Arial, Helvetica, sans-serif;
    font-size: 1em;
    color: #333;
    text-align: center;
    line-height: 60px;
  }

  .el-aside {
    background-color: #ffffff;
    color: #333;
    text-align: center;
    line-height: 200px;
  }

  .el-main {
    background-color: #ffffff;
    color: #333;
    text-align: center;
    line-height: 160px;
  }
}
</style>
