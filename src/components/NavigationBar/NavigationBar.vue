<template>
  <div>
    <!--导航栏-->
    <el-menu mode="horizontal" active-text-color="#59acfe" class="dis-flex" @select="handleSelect">
      <div class="layout-logo">我的笔记</div>
      <el-submenu index="newBuild">
        <template slot="title">新建</template>
        <el-menu-item index="markDown" @click="clickMarkDown">Markdown</el-menu-item>
        <el-menu-item index="doodle">涂鸦</el-menu-item>
      </el-submenu>
      <el-submenu index="all">
        <template slot="title">全部</template>
        <el-menu-item index="work">工作</el-menu-item>
        <el-menu-item index="life">生活</el-menu-item>
        <el-menu-item index="study">学习</el-menu-item>
      </el-submenu>
      <div class="layout-input ">
        <el-input placeholder="输入搜索词"/>
      </div>
    </el-menu>
  </div>
</template>

<script>
import DialogBox from '../common/DialogBox'

export default {
  name: 'NavigationBar',
  components: {DialogBox},
  methods: {
    clickMarkDown () {
      this.$refs.dialogBox.showDialogBox()
    },
    handleSelect (key, keyPat) {
    }
  }
}
</script>

<style scoped>
  .layout-logo {
    width: 100px;
    line-height: 60px;
    float: left;
  }

  .layout-input {
    width: 200px;
    border-radius: 3px;
    line-height: 60px;
    float: right;
  }
</style>
