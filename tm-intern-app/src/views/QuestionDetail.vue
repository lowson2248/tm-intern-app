<template>
  <div class="questionDetail">
    <h2>アンケート詳細</h2>
    <div class="questionHead">
      <!-- 12/17メモ by Iwase
        データ内の情報（アンケートの詳細や結果など）を表示する。
        EDITボタンを押した場合、フラグかなんかで編集モードへ。
        当ページの表示項目としては
          ・アンケート名
          ・アンケート日
          ・アンケ種類
          ・返答数
          ・集計結果（未集計なら非表示）
        がいるかな？
        フォントダサいんで、何とか変えてください。
       -->
      <h1 class="title">{{ discription }}</h1>
      <p class="common">実施日 : <span class="date">{{ date }}</span></p>
      <p class="common">アンケート種別 : <span class="kind">{{ kind }}</span></p>
    </div>
    <div class="questionData">
    </div>
    <div class="questionNav">
      <el-button type="warning" class="el-icon-circle-plus-outline icon">EDIT</el-button>
      <el-button type="danger" class="el-icon-circle-plus-outline icon">DELETE</el-button>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
export default {
  name: 'questionDetail',
  data() {
    return {
        id: 0,
        kind: 'インターン',
        date: '2020-01-01',
        discription: '第N回 1dayインターンアンケート'
    }//return end
  }//data end
}//END
</script>
<style scoped>
.questionDetail{
  width:100%;
  text-align:center;
}

.common{
  font-size:20px;
  font-weight: bold;
}

.questionData{
  width:80%;
  height:70%;
  background:#111;
}


</style>