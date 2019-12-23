<template>
  <div class="question">
    <h2>アンケート管理画面</h2>
    <el-button type="primary" class="el-icon-circle-plus-outline icon">CREATE</el-button>
    
    <div class="questions">
      <el-table :data="tableData" stripe>
        <el-table-column
          prop="isAgg"
          label="Aggregate"
          width="300px">
          <el-button v-if="isAgg" type="warning" class="el-icon-s-marketing icon">OK</el-button>
        </el-table-column>
        <el-table-column
          prop="date"
          label="Date"
          sortable>
        </el-table-column>
        <el-table-column
          prop="discription"
          label="Discription">
        </el-table-column>
        <el-table-column>
          <el-button type="primary" class="el-icon-edit-outline icon">EDIT</el-button>
          <el-button type="danger" class="el-icon-delete icon">DELETE</el-button>
        </el-table-column>
      </el-table>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
export default {
  name: 'question',
  data() {
    return {
      dispray: false,
      tableData: [{
        isAgg: true,
        date: '2020-01-01',
        discription: '第N回 1dayインターンアンケート'
      }, {
        isAgg: false,
        date: '2020-01-02',
        discription: '適当'
      }, {
        isAgg: false,
        date: '2020-01-03',
        discription: '新卒採用内活動方針アンケート'
      }, {
        isAgg: false,
        date: '2020-01-04',
        discription: '新卒採用アンケート'
      }]//tableData end
    }//return end
  }
}
</script>
<style scoped>
.questions{
}

</style>
