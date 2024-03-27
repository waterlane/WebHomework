<template>
  <div>
    <h2 >尝试一下：</h2>
  </div>
  <div class="trans">
    <!-- <input v-model="num" type="number" placeholder="请输入一个整数"> -->
    <el-input v-model="num" style="width: 320px" placeholder="请输入一个整数" />
    <el-button type="primary" @click="convert">转换</el-button>
    <br>
    <p>原码:{{ original }}</p>
    <p >反码:{{ inverse }}</p>
    <p>补码:{{ complement }}</p>
    <!-- <p>二进制: {{ binary }}</p> -->
  </div>
</template>

<script>
export default {
  name: 'Trans',
  data() {
    return {
      num: 0,
      // binary: '',
      original: '00000000000000000000000000000000',
      inverse: '00000000000000000000000000000000',
      complement: '00000000000000000000000000000000'
    };
  },
  methods: {
    convert() {
      let num = this.num;
      let binary = (num >>> 0).toString(2);
      // print(binary);
      this.complement = binary.padStart(32, '0');
      let reverse = (parseInt(this.complement, 2)-1).toString(2).padStart(31, '0');
      this.inverse = num < 0 ?'1'+ reverse : this.complement;
    this.original = num < 0 ?'1' +reverse.split('').map(bit => bit === '1' ? '0' : '1').join('') : this.complement;
  }
  }
};
</script>

<style scoped>
/* 在这里添加你的样式 */
p{
  font-size: large;
  color: #606266;
  font-family:"Gill Sans", sans-serif ;
  /* text-align-last: justify;
  width: 400px; */
}
.trans{
  /* margin: 0 auto; */
  width: 50%;
  /* text-align: center; */
}
h2{
  color:#303133;
}
</style>