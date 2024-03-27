<template>
     <el-col :span="20">
      <h5 class="mb-2" >板块</h5>
      <el-menu
        default-active="2"
        class="el-menu-vertical-demo h-screen"
        @open="handleOpen"
        @close="handleClose"
      ><el-menu-item index="5" @click="$emit('menu-item-selected', 'intro')">
          <el-icon><HomeFilled/></el-icon>
          <span>主页</span>
        </el-menu-item>
        <el-sub-menu index="1">
          <template #title>
            <el-icon><icon-menu /></el-icon>
            <span>数的存储：补码</span>
          </template>
            <el-menu-item index="1-1" @click="$emit('menu-item-selected', 'bit')">整数</el-menu-item>
            <el-menu-item index="1-2" @click="$emit('menu-item-selected', 'float')">浮点数</el-menu-item>
        </el-sub-menu>
        <el-sub-menu index="2">
          <template #title>
            <el-icon><icon-menu /></el-icon>
            <span>指令集</span>
          </template>
            <el-menu-item index="2-1" @click="$emit('menu-item-selected', 'instset')">指令集</el-menu-item>
            <el-menu-item index="2-2" @click="$emit('menu-item-selected', 'inst')">指令</el-menu-item>
            <el-menu-item index="2-3" @click="$emit('menu-item-selected', 'risc')">RISC-V</el-menu-item>
        </el-sub-menu>
        <el-sub-menu index="3">
          <template #title>
            <el-icon><icon-menu /></el-icon>
            <span>计算机底层相关</span>
          </template>
            <el-menu-item index="3-1" @click="$emit('menu-item-selected', 'open')">计算机启动</el-menu-item>
            <el-menu-item index="3-2" @click="$emit('menu-item-selected', 'memo')">内存分段</el-menu-item>
            <!-- <el-menu-item index="3-3" @click="$emit('menu-item-selected', 'compute')">处理器计算</el-menu-item> -->
        <el-sub-menu idex=1>
          <template #title>
            <span>处理器I/O</span>
          </template>
          
            <el-menu-item index="3-4" @click="$emit('menu-item-selected', 'io')">I/O</el-menu-item>
            <el-menu-item index="3-5" @click="$emit('menu-item-selected', 'pio')">PIO</el-menu-item>
            <el-menu-item index="3-6" @click="$emit('menu-item-selected', 'interrupt')">中断</el-menu-item>
          <el-menu-item index="3-7" @click="$emit('menu-item-selected', 'dma')">DMA</el-menu-item>
        </el-sub-menu>
        </el-sub-menu>
        <el-sub-menu index="4">
          <template #title>
            <el-icon><icon-menu /></el-icon>
            <span>编译与汇编</span>
          </template>
            <el-menu-item index="4-1" @click="$emit('menu-item-selected', 'compilation')">编译过程</el-menu-item>
            <!-- <el-menu-item index="4-2" @click="$emit('menu-item-selected', 'memo')">内存分段</el-menu-item> -->
            <el-menu-item index="4-2" @click="$emit('menu-item-selected', 'jump')">JUMP指令</el-menu-item>
            <el-menu-item index="4-3" @click="$emit('menu-item-selected', 'med')">中间代码</el-menu-item>
            <el-menu-item index="4-4" @click="$emit('menu-item-selected', 'jbc')">Java字节码</el-menu-item>
        </el-sub-menu>
        
      </el-menu>
    </el-col>
</template>
<script lang="ts" setup>
import {
  Document,
  Menu as IconMenu,
  Location,
  Setting,
} from '@element-plus/icons-vue'
import { HomeFilled } from '@element-plus/icons-vue';
import type { el } from 'element-plus/lib/locale/index.js';
const handleOpen = (key: string, keyPath: string[]) => {
  console.log(key, keyPath)
}
const handleClose = (key: string, keyPath: string[]) => {
  console.log(key, keyPath)
}
</script>
<style>

.mb-2{
  text-align: center;
}
</style>