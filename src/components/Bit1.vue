<template>
    <div class="complement-code">
      <h1 class="title">补码</h1>
      <p class="subtitle">数在计算机中的存储方式</p>
      <div class="intro">
        <p class="description">
          <span class="highlight">二进制补码</span>是数在计算机中的储存方式，补码用一下规则得出：
        </p>
        <h2 class="example-title">Example</h2>
      </div>
      <div class="content">
        <div class="explanation">
          <div class="rules">
            <p>
              <span class="term">原码</span>：把数的数字部分转换为二进制并在前添加<span class="symbol">符号位</span>（正数为0负数为1）<br />
              <span class="term">反码</span>：正数为<span class="term">原码</span>，负数<span class="term">原码</span>符号位不变，其余位置按位取反<br />
              <span class="term">补码</span>：正数为<span class="term">原码</span>，负数为<span class="term">反码+1</span><br />
            </p>
          </div>
        </div>
        <div class="image-container">
          <img src="https://cdn.builder.io/api/v1/image/assets/TEMP/965fb150f9aa2160a867515d59ae46d1ba6ae2b96cd8d8587a8e8f287e48c51a?apiKey=39ef6d05dc2a469bbef7cd6e8cbc4180&" alt="Complement code example" class="example-image" />
        </div>
      </div>
    </div>
  </template>
  
  <style scoped>
  .complement-code {
    background-color: #fff;
    display: flex;
    flex-direction: column;
    align-items: start;
    padding: 0 80px 80px;
  }
  
  @media (max-width: 991px) {
    .complement-code {
      padding: 0 20px;
    }
  }
  
  .title {
    color: var(--Color-Text-text-color-primary, #303133);
    margin-left: 15px;
    font: 700 64px Inter, sans-serif;
  }
  
  @media (max-width: 991px) {
    .title {
      margin-left: 10px;
      font-size: 40px;
    }
  }
  
  .subtitle {
    color: var(--Color-Text-text-color-regular, #606266);
    margin: 8px 0 0 15px;
    font: 400 16px/150% Inter, sans-serif;
  }
  
  @media (max-width: 991px) {
    .subtitle {
      margin-left: 10px;
    }
  }
  
  .intro {
    display: flex;
    width: 840px;
    max-width: 100%;
    gap: 20px;
    margin: 65px 0 0 15px;
  }
  
  @media (max-width: 991px) {
    .intro {
      flex-wrap: wrap;
      margin-top: 40px;
    }
  }
  
  .description {
    color: var(--Color-Text-text-color-regular, #606266);
    flex-grow: 1;
    flex-basis: auto;
    margin: auto 0;
    font: 400 24px Inter, sans-serif;
  }
  
  @media (max-width: 991px) {
    .description {
      max-width: 100%;
    }
  }
  
  .example-title {
    color: var(--Color-Text-text-color-primary, #303133);
    flex-grow: 1;
    flex-basis: auto;
    font: 700 30px Inter, sans-serif;
  }
  
  .content {
    align-self: center;
    margin-top: 17px;
    width: 100%;
    max-width: 1390px;
    display: flex;
    gap: 20px;
  }
  
  @media (max-width: 991px) {
    .content {
      max-width: 100%;
      flex-direction: column;
      align-items: stretch;
      gap: 0;
    }
  }
  
  .explanation {
    width: 50%;
    margin-left: 0;
  }
  
  @media (max-width: 991px) {
    .explanation {
      width: 100%;
    }
  }
  
  .rules {
    color: var(--Color-Error-color-error-dark-2, #c45656);
    margin-top: 39px;
    font: 400 24px Inter, sans-serif;
  }
  
  @media (max-width: 991px) {
    .rules {
      max-width: 100%;
      margin-top: 40px;
    }
  }
  
  .image-container {
    width: 50%;
    margin-left: 20px;
  }
  
  @media (max-width: 991px) {
    .image-container {
      width: 100%;
    }
  }
  
  .example-image {
    aspect-ratio: 2.04;
    object-fit: auto;
    object-position: center;
    width: 100%;
    flex-grow: 1;
  }
  
  @media (max-width: 991px) {
    .example-image {
      max-width: 100%;
      margin-top: 40px;
    }
  }
  
  .highlight {
    color: rgba(64, 158, 255, 1);
  }
  
  .term {
    color: rgba(64, 158, 255, 1);
  }
  
  .symbol {
    color: rgba(196, 86, 86, 1);
  }
  </style>