<template>

    <div class="menu" >
      <Menu></Menu>
      
  <Introduce v-if="IntroMsg"></Introduce> 
  <Bit v-if="ShowBit"></Bit>

  </div>
   
</template>

<script>
import Menu from "./components/Menu.vue"
import Introduce from "./components/Introduce.vue"
import Bit from "./components/Bit.vue"
export default{
  components:{
Menu,
Introduce,
Bit
  },
  
    data(){
      return{
        IntroMsg : false,//介绍界面
        ShowBit: true,//二进制、浮点数、指令集
        ShowMemo:false,//内存为中心
        ShowJump:false,//JUMP
        ShowComp:false,//编译原理
        ShowInst:false,//指令集
        ShowMed:false,//中间代码
        ShowOpen:false//x86计算机开机地址规范 开机过程
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
