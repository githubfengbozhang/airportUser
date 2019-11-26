<template>
  <div class="home">
    <el-row class="home-box">
      <el-row>
        <el-col :span="24">
          <div>
            <span>
              回国流量包（32G）
            </span>
            <span>
              有效期：2019/10/10 10:00:00
            </span>
          </div>
        </el-col>
      </el-row>
      <div class="borderLine" />
      <el-row>
        <el-col :span="24">
          <div>
            <span>
              套餐（32G）
            </span>
            <span>
              2019/9/10 10:00:00~2019/10/10 10:00:00
            </span>
          </div>
          <el-row :gutter="20" class="home-progress">
            <el-col :span="16"><el-progress :text-inside="true" :stroke-width="18" :percentage="70" /></el-col>
            <el-col :span="8"><span>4GB13.87M/32GB</span></el-col>
          </el-row>
        </el-col>
        <el-col :span="24" class="remove-padding-top">
          <div>
            <span>
              套餐（32G）
            </span>
            <span>
              2019/9/10 10:00:00~2019/10/10 10:00:00
            </span>
          </div>
          <el-row :gutter="20" class="home-progress">
            <el-col :span="16"><el-progress :text-inside="true" :stroke-width="18" :percentage="80" /></el-col>
            <el-col :span="8"><span>4GB13.87M/32GB</span></el-col>
          </el-row>
        </el-col>
      </el-row>
    </el-row>
    <el-row class="home-box remove-padding-top">
      <el-row>
        <el-col :span="24">
          <div>
            <span>
              高速流量包（32G）
            </span>
            <span>
              已过期
            </span>
            <a class="home-box-buy">购买</a>
          </div>
        </el-col>
      </el-row>
      <div class="borderLine" />
      <el-row>
        <el-col :span="24">
          <div>
            <span>
              套餐（32G）
            </span>
            <span>
              2019/9/10 10:00:00~2019/10/10 10:00:00
            </span>
          </div>
          <el-row :gutter="20" class="home-progress">
            <el-col :span="16"><el-progress :text-inside="true" :stroke-width="18" :percentage="70" /></el-col>
            <el-col :span="8"><span>4GB13.87M/32GB</span></el-col>
          </el-row>
        </el-col>
        <el-col :span="24" class="remove-padding-top">
          <div>
            <span>
              套餐（32G）
            </span>
            <span>
              2019/9/10 10:00:00~2019/10/10 10:00:00
            </span>
          </div>
          <el-row :gutter="20" class="home-progress">
            <el-col :span="16"><el-progress :text-inside="true" :stroke-width="18" :percentage="80" /></el-col>
            <el-col :span="8"><span>4GB13.87M/32GB</span></el-col>
          </el-row>
        </el-col>
      </el-row>
    </el-row>
    <el-row class="home-box remove-padding-top">
      <el-row>
        <el-row type="flex" class="row-bg" justify="space-between">
          <el-col :span="19">
            <span style="line-height:40px">我的邀请</span>
          </el-col>
          <el-col :span="5">
            <span>
              邀请码：GBK11201
            </span>
            <el-button type="primary">复制</el-button>
          </el-col>
        </el-row>
      </el-row>
      <div class="borderLine" />
      <el-row>
        <el-col :span="24">
          <!-- <el-row type="flex" class="row-bg" justify="center">
            <el-col :span="6">
              <span>邀请好友，可获得礼券，<a>查看规则</a></span>
            </el-col>
          </el-row> -->
          <el-row>
            <span>已邀请：5人</span>
            <span>激活：4人</span>
            <el-table
              :data="tableData"
              border
              style="width: 100%"
            >
              <el-table-column
                prop="date"
                label="邀请用户"
                width="180"
              />
              <el-table-column
                prop="name"
                label="注册时间"
                width="180"
              />
              <el-table-column
                prop="address"
                label="购买套餐"
              />
              <el-table-column
                prop="address"
                label="激活时间"
              />
              <el-table-column
                prop="address"
                label="状态"
              />
            </el-table>
          </el-row>
        </el-col>
      </el-row>
    </el-row>
  </div>
</template>
<script>
export default {
  data() {
    return {
      tableData: [{
        date: '2016-05-02',
        name: '王小虎',
        address: '上海市普陀区金沙江路 1518 弄'
      }, {
        date: '2016-05-04',
        name: '王小虎',
        address: '上海市普陀区金沙江路 1517 弄'
      }, {
        date: '2016-05-01',
        name: '王小虎',
        address: '上海市普陀区金沙江路 1519 弄'
      }, {
        date: '2016-05-03',
        name: '王小虎',
        address: '上海市普陀区金沙江路 1516 弄'
      }]
    }
  }
}
</script>
<style lang="scss" scoped>
  .home{
    &-box{
      padding: 20px 15px;
      &-buy{
        color: red
      }
      .el-row{
        background-color: white;
        .el-col{
          padding: 20px 15px
        }
      }
      .borderLine{
        padding: 0 15px;
        border-bottom: 1px solid #F2F2F2
      }
    }
    .remove-padding-top{
        padding-top: 0 !important
    }
    &-progress{
      padding-top: 15px
    }
  }
</style>
