<template>
  <div class="hello">
      <!--表格-->
      <el-table
      :data="tableData"
      style="width: 100%">
      <el-table-column
        prop="date"
        label="出生日期"
        align="center"
        >
      </el-table-column>
      <el-table-column
        prop="name"
        label="姓名"
        align="center"
        >
      </el-table-column>
      <el-table-column
        prop="address"
        label="籍贯"
        align="center"
        >
      </el-table-column>
    </el-table>

    <!--分页-->
    <el-row style="padding:10px 20px;background:#f5f5f5">
       <el-col :span="12">
          <el-pagination
          @size-change="handleSizeChange"
          @current-change="handleCurrentChange"
          :current-page="1"
          :page-sizes="[2, 5, 10, 20]"
          :page-size="100"
          layout="total, sizes, prev, pager, next, jumper"
          :total="400">
        </el-pagination>
       </el-col>
    </el-row>
  </div>
</template>

<script>
/**
 * 要求：根据原始数据data，完成分页和调整每页数量的功能
 */
import data from '@/data.js'
export default {
  name: "list",
  data() {
    return {
      tableData: data
    };
  },
  methods: {
    handleSizeChange(val){

    },
    handleCurrentChange(val){

    },
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1,
h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
