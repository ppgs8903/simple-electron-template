<template>
  <div class="toolbar">
    <el-dropdown>
      <el-icon style="margin-right: 8px; margin-top: 1px"><setting /></el-icon>
      <template #dropdown>
        <el-dropdown-menu>
          <el-dropdown-item @click="toPage('/')">Home</el-dropdown-item>
          <el-dropdown-item @click="toPage('/About')">About</el-dropdown-item>
        </el-dropdown-menu>
      </template>
    </el-dropdown>
    <span>Tom</span>
  </div>
</template>

<script>
export default {
  methods: {
    toPage(pg) {
      this.$router.push(pg)
    }
  }
};
</script>
