<template>
  <div>
    <el-container class="project-main">
      <el-header class="header">子部件信息</el-header>
      <el-main>
        <div class="main">
          <el-form ref="form"  label-width="100px">
            <el-form-item label="子部件名称">
              <el-col :span="10">
                <el-input ></el-input>
              </el-col>
            </el-form-item>
            <el-form-item label="截止时间">
              <el-col :span="10">
                <el-date-picker type="date" placeholder="选择日期" style="width: 100%;"></el-date-picker>
              </el-col>
            </el-form-item>
            <el-form-item label="物料编码">
              <el-col :span="10">
                <el-input ></el-input>
              </el-col>
            </el-form-item>
            <el-form-item label="子部件进度">
              <el-collapse accordion>
                <el-collapse-item title="分单">
                 <el-form>
                  <el-form-item label="分单1"></el-form-item>
                    <el-steps :space="100" :active="1" finish-status="success">
                      <el-step title="完成"></el-step>
                      <el-step title="建设中"></el-step>
                      <el-step title="未完成"></el-step>
                    </el-steps>
                  <el-form-item label="分单2"></el-form-item>
                    <el-steps :space="100" :active="0" finish-status="success">
                      <el-step title="建设中"></el-step>
                      <el-step title="未完成"></el-step>
                      <el-step title="未完成"></el-step>
                    </el-steps>
                </el-form>
                </el-collapse-item>
              </el-collapse>
            </el-form-item>
            <el-form-item label="开始时间">
              <el-col :span="11">
                <el-date-picker type="date" placeholder="选择日期"  style="width: 100%;"></el-date-picker>
              </el-col>
            </el-form-item>
            <el-form-item label="子部件备注">
              <el-input type="textarea" ></el-input>
            </el-form-item>
          </el-form>
        </div>
      </el-main>
    </el-container>
  </div>
</template>

<script>
export default {
  name: 'ProjectPart',
  data () {
    return {
      date: ''
    }
  }
}
</script>
<style scoped>
  .project-main {
    margin-top: -20px;
  }
  .header {
    text-align: center;
    font-size: 24px;
    line-height: 60px;
    background: #fff;
    border-bottom: #eee 1px solid;
    margin-top: -10px;
  }
  .main {
    position: relative;
    width: 100%;
  }
</style>