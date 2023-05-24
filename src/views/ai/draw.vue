<template>

  <div>
    <el-row style="margin:5px 0 ">
      <el-card style="display: flex; justify-content: center;">
        <el-tag type="success" effect="plain" style="font-size:22px">AI绘画</el-tag>
      </el-card>
    </el-row>
    <el-row>
      <el-col :span="12">
        <el-card >
          <el-form :model="formData" ref="vForm" :rules="rules" label-position="left" label-width="80px" size="medium"
                   @submit.native.prevent>
            <el-form-item label="输入描述" prop="textarea62680" class="label-center-align">
              <el-input type="textarea" v-model="formData.textarea62680" rows="3"></el-input>
            </el-form-item>
            <el-form-item label="图片风格" prop="select112587">
              <el-select v-model="formData.select112587" class="full-width-input" clearable>
                <el-option v-for="(item, index) in select112587Options" :key="index" :label="item.label"
                           :value="item.value" :disabled="item.disabled"></el-option>
              </el-select>
            </el-form-item>
            <el-form-item label="图片规格" prop="select98470">
              <el-select v-model="formData.select98470" class="full-width-input" clearable>
                <el-option v-for="(item, index) in select98470Options" :key="index" :label="item.label"
                           :value="item.value" :disabled="item.disabled"></el-option>
              </el-select>
            </el-form-item>

            <el-row style="display: flex; justify-content: center;">
              <el-button>重置</el-button>
              <el-button type="primary">提交</el-button>
            </el-row>


          </el-form>
        </el-card>

      </el-col>
      <el-col :span="12">
        <el-card class="demo-image__error">
          <div class="block">
            <div class="demonstration" style="margin-bottom: 5px">生成的图片</div>
            <div style="height: 230px; border: 1px solid ;">
              <el-image>
                <div slot="error" class="image-slot">
                  <i class="el-icon-picture-outline"></i>
                </div>
              </el-image>
            </div>

          </div>
        </el-card>
      </el-col>
    </el-row>

  </div>

</template>

<script>
export default {
  name: "draw",
  data() {
    return {
      formData: {
        textarea62680: "",
        select112587: 2,
        select98470: "",
      },
      rules: {},
      select112587Options: [{
        "label": "select 2",
        "value": 2
      }],
      select98470Options: [{
        "label": "select 1",
        "value": 1
      }, {
        "label": "select 2",
        "value": 2
      }, {
        "label": "select 3",
        "value": 3
      }],
    }
  },
}
</script>

<style scoped>

</style>
