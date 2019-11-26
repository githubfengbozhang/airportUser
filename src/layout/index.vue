<template>
  <!-- <div :class="classObj" class="app-wrapper">
    <div v-if="device==='mobile'&&sidebar.opened" class="drawer-bg" @click="handleClickOutside" />
    <sidebar class="sidebar-container" />
    <div class="main-container">
      <div :class="{'fixed-header':fixedHeader}">
        <navbar />
      </div>
      <app-main />
    </div>
  </div> -->
  <el-container>
    <el-header> <navbar /></el-header>
    <el-row type="flex" class="row-bg" justify="center">
      <el-col :span="2">
        <el-aside style="padding-top: 20px"><sidebar /></el-aside>
      </el-col>
      <el-col :span="18"><app-main /></el-col>
    </el-row>
  </el-container>
</template>

<script>
// import { Navbar, Sidebar, AppMain } from './components'
import { Navbar, Sidebar, AppMain } from './components'
import ResizeMixin from './mixin/ResizeHandler'

export default {
  name: 'Layout',
  components: {
    Navbar,
    Sidebar,
    AppMain
  },
  mixins: [ResizeMixin],
  computed: {
    sidebar() {
      return this.$store.state.app.sidebar
    },
    device() {
      return this.$store.state.app.device
    },
    fixedHeader() {
      return this.$store.state.settings.fixedHeader
    },
    classObj() {
      return {
        hideSidebar: !this.sidebar.opened,
        openSidebar: this.sidebar.opened,
        withoutAnimation: this.sidebar.withoutAnimation,
        mobile: this.device === 'mobile'
      }
    }
  },
  methods: {
    handleClickOutside() {
      this.$store.dispatch('app/closeSideBar', { withoutAnimation: false })
    }
  }
}
</script>

<style lang="scss" scoped>
 .row-bg{
   background-color: #EBEEF5
  }
 .container{
    background-color: #EBEEF5
  }
  .el-header{
    padding: 0;
  }
</style>
