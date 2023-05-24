<template>
  <div>


    <el-row>
      <el-input class="search-input" placeholder="请输入使用场景"
                clearable
                prefix-icon="el-icon-search" v-model="searchText"/>
    </el-row>

    <el-row style="margin: 0  3%">
      <el-tabs v-model="activeName" @tab-click="handleClick">
        <el-tab-pane label="全部" name="first">

          <el-row>
            <el-col :span="3">
              <itemCard></itemCard>
            </el-col>
          </el-row>

        </el-tab-pane>

        <!--      <el-tab-pane label="画图" name="second">-->
        <!--          -->
        <!--      </el-tab-pane>-->
      </el-tabs>

    </el-row>

  </div>
</template>

<script>
import {mapGetters} from 'vuex'
import itemCard from "@/views/home/itemCard.vue";

export default {
  name: 'Home',
  components: {
    itemCard,
  },
  computed: {
    ...mapGetters([
      'name'
    ])
  },
  data() {
    return {
      searchText: '', // 搜索框的内容
      activeName: 'first'
    };
  },
}
</script>


<style lang="scss" scoped>

.search-input {
  width: 90%;
  margin: 20px
}
</style>
