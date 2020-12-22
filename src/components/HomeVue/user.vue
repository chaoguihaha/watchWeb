<template>
  <div>
    <el-button type="primary" @click="addUser()">添加用户</el-button>
    <el-button type="primary" @click="queryUser()" style="float: right;">搜索</el-button>
    <el-input v-model="param" placeholder="请输入搜索内容" style="float: right; width: 300px; margin-bottom: 20px"></el-input>
    <el-table
        ref="singleTable"
        :data="tableData"
        highlight-current-row
        @current-change="handleCurrentChange"
        style="width: 100%">
      <el-table-column
          type="index"
          width="50">
      </el-table-column>
      <el-table-column
          property="date"
          label="账号"
          width="120">
      </el-table-column>
      <el-table-column
          property="name"
          label="密码"
          width="120">
      </el-table-column>
      <el-table-column
          property="address"
          label="openid">
      </el-table-column>
      <el-table-column
          property="address"
          label="用户类型">
      </el-table-column>
      <el-table-column
          property="address"
          label="操作">
        <el-tooltip class="item" effect="dark" content="编辑" placement="top-start">
          <el-button type="primary" icon="el-icon-edit" circle @click="updateUser()"></el-button>
        </el-tooltip>
        <el-tooltip class="item" effect="dark" content="绑定信息" placement="top-start">
          <el-button type="warning" icon="el-icon-star-off" circle></el-button>
        </el-tooltip>
        <el-tooltip class="item" effect="dark" content="删除" placement="top-start">
          <el-button type="danger" icon="el-icon-delete" circle @click="deleteUser()"></el-button>
        </el-tooltip>
      </el-table-column>
    </el-table>
  </div>
</template>

<script>
export default {
  name: "user",
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
      }],
      currentRow: null,
      param: ""
    }
  },

  methods: {
    handleCurrentChange(val) {
      this.currentRow = val;
    },
    queryUser(){
      console.log(this.param);
    },
    addUser() {

    },
    updateUser() {

    },
    deleteUser() {

    }
  }
}
</script>

<style scoped>

</style>