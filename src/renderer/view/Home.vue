<template>
  <el-main>
    <el-scrollbar>
      <el-table :data="tableData">
        <el-table-column prop="date" label="Date" width="140" />
        <el-table-column prop="name" label="Name" width="120" />
        <el-table-column prop="address" label="Address" />
      </el-table>
    </el-scrollbar>
  </el-main>
</template>

<script>
import LeftMenu from "../component/LeftMenu.vue";
import TopMenu from "../component/TopMenu.vue";

export default {
  components: {
    LeftMenu,
    TopMenu,
  },
  data() {
    const item = {
      date: "2016-05-02",
      name: "Tom",
      address: "No. 189, Grove St, Los Angeles",
    };
    const tableData = Array.from({ length: 20 }).fill(item);
    return {
      tableData: tableData,
    };
  },
  methods: {},
  mounted() {},
};
</script>

<!-- <script setup>
    import {
      ref,
      reactive,
      toRefs,
    } from 'vue'

    const data = reactive({
      patternVisible: false,
      debugVisible: false,
      aboutExeVisible: false,
    })

    const message = ref('content')
</script> -->

<style scoped></style>
