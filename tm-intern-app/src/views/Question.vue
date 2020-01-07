<template>
  <div class="questionPage">
    <h2>アンケート管理画面</h2>
    <el-button type="success" class="el-icon-circle-plus-outline icon" href="QuestionDetail">CREATE</el-button>
    
    <div class="questions">
      <el-table :data="tableData" stripe>
        <!-- 12/27メモ by Iwase
          ・作成ボタン（CREATE）で作成画面へ遷移
          ・対象アンケートをクリックで該当アンケートの詳細画面へ遷移（方法模索中、idを渡してやるのがいいかも？）
          ・アンケートに種類を追加（インターンと採用とカスタム）
          ・日付とアンケート種類でソート可能
        -->
        <el-table-column
          prop="date"
          label="Date"
          sortable
        >
        </el-table-column>
        <el-table-column
          prop="kind"
          label="Kind"
          sortable
        >
        </el-table-column>
        <el-table-column
          prop="discription"
          label="Discription"
        >
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
      tableData: [{
        id: 0,
        kind: 'インターン',
        date: '2020-01-01',
        discription: '第N回 1dayインターンアンケート'
      }, {
        id: 1,
        kind: 'カスタム',
        date: '2020-01-02',
        discription: '適当'
      }, {
        id: 2,
        kind: 'カスタム',
        date: '2020-01-03',
        discription: '新卒採用内活動方針アンケート'
      }, {
        id: 3,
        kind: '採用',
        date: '2020-01-04',
        discription: '新卒採用アンケート'
      }]//tableData end
    }//return end
  },
  methods: {
    select(some){
      console.log('id is' + some.id)
    }//select end
  }
}//END
</script>
<style scoped>
</style>
