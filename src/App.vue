<template>

  <div class="common-layout" width="100vh">
    <el-container>
      <!-- <el-header>Header</el-header> -->
      <el-container>
        <el-aside width="20%">
          <Menu @menu-item-selected="handleMenuItemSelected"></Menu>
        </el-aside>
        <el-main>
          <Introduce v-if="IntroMsg"/>
  <Bit v-if="ShowBit"/>
  <Float v-if="ShowFloat"/>
  <InstSet v-if="ShowInstSet"/>
  <Inst v-if="ShowInst"/>
  <RISC v-if="ShowRISC"/>
  <Open v-if="ShowOpen"/>
  <Memo v-if="ShowMemo"/>
  <Compilation v-if="ShowComp"/>
  <JUMP v-if="ShowJump"/>
  <!-- <Trans v-if="ShowBit"></Trans> -->
        </el-main>
        <!-- <el-footer>Footer</el-footer> -->
      </el-container>
    </el-container>
  </div>

    <!--<div class="menu" >
      <Menu></Menu>
      
  <Introduce v-if="IntroMsg"></Introduce> 
  <Bit v-if="ShowBit"></Bit>

  </div>-->
   
</template>


<script >
import Menu from "./components/Menu.vue"
import Introduce from "./components/Introduce.vue"
import Bit from "./components/Bit.vue"
import Trans from "./components/Trans.vue"
import Float from "./components/Float.vue"
import InstSet from "./components/InstSet.vue"
import Inst from "./components/Inst.vue"
import RISC from "./components/RISC.vue"
import Open from "./components/Open.vue"
import Memo from "./components/Memo.vue"
import { th } from "element-plus/es/locale/index.mjs"
import Compilation from "./components/Compilation.vue"
import JUMP from "./components/JUMP.vue"
export default{
  components:{
Menu,
Introduce,
Bit,
Trans,
Float,
InstSet,
Inst,
RISC,
Open,
Memo,
Compilation,
JUMP
  },
  
    data(){
      return{
        IntroMsg : true,//介绍界面
        ShowBit: false,//二进制、浮点数、指令集
        ShowFloat:false,//浮点数
        ShowMemo:false,//内存为中心
        ShowJump:false,//JUMP
        ShowComp:false,//编译原理
        ShowInstSet:false,//指令集
        ShowRISC:false,//RISC-V
        ShowInst:false,//指令
        ShowMed:false,//中间代码
        ShowOpen:false//x86计算机开机地址规范 开机过程
      }
    },
    methods: {
  handleMenuItemSelected(menuItem) {
    this.IntroMsg = menuItem === 'intro';
    this.ShowBit = menuItem === 'bit';
    this.ShowFloat = menuItem === 'float';
    this.ShowMemo = menuItem === 'memo';
    this.ShowJump = menuItem === 'jump';
    this.ShowComp = menuItem === 'compilation';
    this.ShowInst = menuItem === 'inst';
    this.ShowInstSet = menuItem === 'instset';
    this.ShowRISC = menuItem === 'risc';
    this.ShowMed = false;
    this.ShowOpen = menuItem === 'open';
  }
}
  
}

</script>

<style scoped>

.menu{
  /* width: 20%; */
  /* width: 50%; */
  height: auto;
  display: flex;
  background-color: #ffffff;
  /* justify-content: space-between; */
  gap: 0;
}


/* h1{
  text-align: center;
}
h3{
  text-align: center;
} */
/* header {
  line-height: 1.5;
} */

/* .logo {
  display: block;
  margin: 0 auto 2rem;
} */

/* @media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  } */
/* 
  .logo {
    margin: 0 2rem 0 0;
  } */
/* 
  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  } */
/* } */
</style>
