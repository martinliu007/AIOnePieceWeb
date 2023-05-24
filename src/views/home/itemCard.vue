<template>
  <div>

    <div @click="openItemDetail" style=" cursor: pointer">
      <el-card class="box-card" >
        <div slot="header" class="clearfix">
          <span class="center-text">AI绘图</span>
        </div>
        <div class="component-item">
          <pan-thumb width="100px" height="100px">
            <i class="fa fa-search center-icon fa-3x"></i>
          </pan-thumb>
        </div>
      </el-card>
    </div>

  </div>
</template>

<script>
export default {
  name: "items",
  methods: {
    openItemDetail() {
      window.open("#/ai/draw", "_blank");
    },
  },
}
</script>

<style lang="scss" scoped>
.center-text {
  display: flex;
  justify-content: center;
}

.center-icon {
  display: flex;
  justify-content: center;
  align-items: center;
}

</style>
