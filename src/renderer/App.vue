<template>
  <el-container class="layout-container-demo" style="height: 500px">
    <el-aside width="200px">
      <LeftMenu />
    </el-aside>

    <el-container>
      <el-header style="text-align: right; font-size: 12px">
        <TopMenu />
      </el-header>

      <el-main>
        <router-view></router-view>
      </el-main>
    </el-container>
  </el-container>
</template>

<script>
import LeftMenu from "./component/LeftMenu.vue"
import TopMenu from "./component/TopMenu.vue"

export default {
  components: {
    LeftMenu,
    TopMenu
  },
  data() {
    const item = {
      date: '2016-05-02',
      name: 'Tom',
      address: 'No. 189, Grove St, Los Angeles',
    }
    const tableData = Array.from({ length: 20 }).fill(item)
    return {
      tableData: tableData,
    };
  },
  methods: {},
  mounted() {},
};
</script>
