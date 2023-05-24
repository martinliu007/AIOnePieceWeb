<template>
  <el-row class="navbar">
    <el-col class="section" :span="2"><span v-if="!fold"><img class="logo" src="@/assets/hello_logo.png" style="width: 50px; height: 50px" /><small class="title">Portal</small></span><i class="action fold-icon" :class="fold ? 'el-icon-s-unfold' : 'el-icon-s-fold'" @click="toggleFold"></i></el-col>
  </el-row>
</template>

<script>
export default {
  name: "topBar"
}
</script>

<style scoped>

</style>
