
   <template><div class="bit"><h1 tabindex="-1">数在计算机里的存储方式:补码</h1>
   <!-- </br> -->
   <el-text class="mx-1" size="extra-large">
    -86<br><br>
  原码：<norb class="operation">1</norb>001010110<br><br>
  反码：<norb class="operation">1</norb>110101001<br><br>
  补码：<norb class="operation">1</norb>110101010<br><br><norb class="operation">符号位</norb></el-text>
   <input >
   </div></template> 
<style>
.bit{
  padding-left: 5%;
  width: 100vh;
}
.text{
  padding-left: 30%;
  font-size: 20px;
  line-height: 20px;
}
.operation{
  background-color:#a0cfff;
  display: inline;
}
</style>
<!-- <template>
  <el-text class="mx-1">Default</el-text>
  <el-text class="mx-1" type="primary">Primary</el-text>
  <el-text class="mx-1" type="success">Success</el-text>
  <el-text class="mx-1" type="info">Info</el-text>
  <el-text class="mx-1" type="warning">Warning</el-text>
  <el-text class="mx-1" type="danger">Danger</el-text>
</template> -->

    <!-- <el-form :model="user_data" :rules="user_rules" ref="ruleForm" label-width="230px" id="user_form">
  <el-row>
    <el-col :span="12">
      <el-form-item label="性别：" prop="gender">
        <el-select
          v-model="user_data.gender"
          style="width: 200px"
          placeholder="请选择"
          @input="handleGenderChange"
        >
          <el-option value="1" label="男"></el-option>
          <el-option value="2" label="女"></el-option>
        </el-select>
      </el-form-item>
    </el-col>
  </el-row>
  <el-row>
    <el-col :span="12">
      <el-form-item label="备注：" prop="bz">
        <el-input
          class="bz"
          v-model="user_data.bz"
          placeholder="必填项"
          @input="handleBzChange"
        ></el-input>
      </el-form-item>
    </el-col>
  </el-row>
   <el-row>
    <el-col :span="12">
      <el-form-item label="用户信息预览：" prop="yhxx">
        <el-input
          type="text"
          class="yhxx"
          v-model="user_data.yhxx"
          :disabled="true"
          :style="{width:text(user_data.yhxx)}"
        ></el-input>
      </el-form-item>
    </el-col>
  </el-row>
 </el-form> -->




<!-- <template>

    <div>
      <el-input
        v-model="input1"
        style="max-width: 600px"
        placeholder="Please input"
      >
        <template #prepend>Http://</template>
      </el-input>
    </div>
    <div class="mt-4">
      <el-input
        v-model="input2"
        style="max-width: 600px"
        placeholder="Please input"
      >
        <template #append>.com</template>
      </el-input>
    </div>
    <div class="mt-4">
      <el-input
        v-model="input3"
        style="max-width: 600px"
        placeholder="Please input"
        class="input-with-select"
      >
        <template #prepend>
          <el-select v-model="select" placeholder="Select" style="width: 115px">
            <el-option label="Restaurant" value="1" />
            <el-option label="Order No." value="2" />
            <el-option label="Tel" value="3" />
          </el-select>
        </template>
        <template #append>
          <el-button :icon="Search" />
        </template>
      </el-input>
    </div>
    <div class="mt-4">
      <el-input
        v-model="input3"
        style="max-width: 600px"
        placeholder="Please input"
        class="input-with-select"
      >
        <template #prepend>
          <el-button :icon="Search" />
        </template>
        <template #append>
          <el-select v-model="select" placeholder="Select" style="width: 115px">
            <el-option label="Restaurant" value="1" />
            <el-option label="Order No." value="2" />
            <el-option label="Tel" value="3" />
          </el-select>
        </template>
      </el-input>
    </div>
  </template>
  
  <script setup lang="ts">
  import { ref } from 'vue'
  import { Search } from '@element-plus/icons-vue'
  const input1 = ref('')
  const input2 = ref('')
  const input3 = ref('')
  const select = ref('')
  </script>
  
  <style>
  .input-with-select .el-input-group__prepend {
    background-color: var(--el-fill-color-blank);
  }
  </style> -->
  

<!-- // const message = ref('');
// export default{
//     //根据内容长度，实时计算预览框的长度
// text(){
// 	return function(value){
// 	  if(value == '' || value == 0){
// 	    return '200px'
// 	  }else{
// 	    return (String(value).length*13+70) + 'px'
// 	  }
// 	}
// }

// //根据性别选择的变化，实时更新内容
// handleGenderChange(item){
//   this.user_data.gender = item == "1"?"男":"女";
//   if(this.user_data.bz.length > 0){
//     this.user_data.yhxx = this.user_data.gender+","+this.user_data.bz;
//   }else{
//     this.user_data.yhxx = this.user_data.gender;
//   }
// },

// //根据输入备注内容的变化，实时更新内容
// handleBzChange(item){
//   this.user_data.bz = item;
//   if(this.user_data.bz.length > 0){
//     this.user_data.yhxx = this.user_data.gender+","+this.user_data.bz;
//   }else{
//     this.user_data.yhxx = this.user_data.gender;
//   }
// }
// } -->

