<template>
  <div class="questionDetail">
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
      <p class="common">実施日 : <span class="date" >{{ date }}</span></p>
      <p class="common">アンケート種別 : <span class="kind">{{ kind }}</span></p>
    </div>
    <div class="questionNav">
      <el-button type="warning" class="el-icon-circle-plus-outline icon" v-on:click="test">EDIT</el-button>
      <el-button type="danger" class="el-icon-circle-plus-outline icon">DELETE</el-button>
    </div>
    <div v-if="editFlg" class="questionData">
      <el-button @click="addItem">New Item</el-button>
      <el-form>
        <el-form-item
          v-for="(item, index) in dynamicValidateForm.items"
          :label="'項目' + ( index + 1 )"
          :key="item.key"
          :prop="'items.' + index + '.value'"
          :rules="{
            required: true, message: 'item can not be null', trigger: 'blur'
          }"
        >
          <el-input v-model="item.value"></el-input><el-button @click.prevent="removeItem(item)">Delete</el-button>
        </el-form-item>
      </el-form>
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
        discription: '第N回 1dayインターンアンケート',
        editFlg: true,
        dynamicValidateForm: {
          items: [{
            key: 1,
            value: ''
          }]
        }
    }//return end
  },//data end
  methods: {
    test(){
      if(this.editFlg == true){
        console.log('true to false')
        this.editFlg = false
      }else{
        console.log('false to true')
        this.editFlg = true
      }
    },
    removeItem(item) {
      var index = this.dynamicValidateForm.items.indexOf(item);
      if (index !== -1) {
        this.dynamicValidateForm.items.splice(index, 1);
      }
    },
    addItem() {
      this.dynamicValidateForm.items.push({
        key: Date.now(),
        value: ''
      });
    }
  }
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
}


</style>