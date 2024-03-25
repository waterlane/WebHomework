<template>
    <main class="floating-point-storage">
      <section class="intro">
        <h1 class="title">补码</h1>
        <p class="subtitle">数在计算机中的存储方式</p>
        <p class="description">
          <span class="highlight">浮点数</span>存储：
        </p>
        <p class="details">
          底(r)<span class="detail-text">：阶码的底，通常为​2</span><br />
          阶码(E)<span class="detail-text">：</span><span class="detail-text">阶码数值，决定数的范围</span><br />
          尾数(M)<span class="detail-text">：决定数的符号和精度</span>
        </p>
        <img src="https://cdn.builder.io/api/v1/image/assets/TEMP/58beb81cf21721cb0fbe4c54d2fed1a9a6a43a4fc2b9c72c423a1afeb2d72760?apiKey=39ef6d05dc2a469bbef7cd6e8cbc4180&" alt="Floating point storage diagram" class="diagram" />
      </section>
      
      <section class="example">
        <h2 class="example-title">Example</h2>
        <div class="example-container">
          <div class="example-content">
            <div class="decimal-representation">
              <p class="decimal-label">十进制：-0.4375</p>
              <img src="https://cdn.builder.io/api/v1/image/assets/TEMP/285bf10360cf267ecc44fbbeaf741366ca56bf5540282bf96ea37f90bd48d3ba?apiKey=39ef6d05dc2a469bbef7cd6e8cbc4180&" alt="Decimal representation" class="decimal-image" />
            </div>
            <p class="binary-representation">
              原码：<span class="binary-highlight">1001</span>1111
            </p>
            <p class="binary-representation">
              反码：<span class="binary-highlight">1110</span>1000
            </p>
            <p class="binary-representation">
              补码：<span class="binary-highlight">1111</span><span class="binary-text">1001</span>
            </p>
          </div>
          <p class="exponent-label">阶码</p>
        </div>
      </section>
    </main>
  </template>
  
  <style scoped>
  .floating-point-storage {
    background-color: #fff;
    display: flex;
    align-items: start;
    gap: 20px;
    justify-content: space-between;
    padding: 0 80px 80px;
  }
  
  @media (max-width: 991px) {
    .floating-point-storage {
      flex-wrap: wrap;
      padding: 0 20px;
    }
  }
  
  .intro {
    display: flex;
    flex-direction: column;
    font-size: 24px;
    color: var(--Color-Text-text-color-regular, #606266);
    font-weight: 400;
  }
  
  .title {
    color: var(--Color-Text-text-color-primary, #303133);
    align-self: start;
    font: 700 64px Inter, sans-serif;
  }
  
  @media (max-width: 991px) {
    .title {
      font-size: 40px;
    }
  }
  
  .subtitle {
    align-self: start;
    margin-top: 8px;
    font: 16px/150% Inter, sans-serif;
  }
  
  .description {
    font-family: Inter, sans-serif;
    margin-top: 68px;
  }
  
  @media (max-width: 991px) {
    .description {
      margin-top: 40px;
    }
  }
  
  .highlight {
    color: rgba(64, 158, 255, 1);
  }
  
  .details {
    font-family: Inter, sans-serif;
    margin-top: 51px;
  }
  
  @media (max-width: 991px) {
    .details {
      margin-top: 40px;
    }
  }
  
  .detail-text {
    color: rgba(96, 98, 102, 1);
  }
  
  .diagram {
    aspect-ratio: 6.25;
    object-fit: auto;
    object-position: center;
    width: 263px;
    align-self: center;
    margin-top: 39px;
    max-width: 100%;
  }
  
  .example {
    display: flex;
    margin-top: 174px;
    flex-direction: column;
  }
  
  @media (max-width: 991px) {
    .example {
      max-width: 100%;
      margin-top: 40px;
    }
  }
  
  .example-title {
    color: var(--Color-Text-text-color-primary, #303133);
    font: 700 30px Inter, sans-serif;
  }
  
  @media (max-width: 991px) {
    .example-title {
      max-width: 100%;
    }
  }
  
  .example-container {
    box-shadow: 0px 12px 32px 4px rgba(0, 0, 0, 0.04), 0px 8px 20px 0px rgba(0, 0, 0, 0.08);
    border: 1px solid rgba(222, 223, 224, 1);
    background-color: var(--Color-Background-bg-color, #fff);
    display: flex;
    margin-top: 29px;
    flex-direction: column;
    color: var(--Color-Error-color-error-dark-2, #c45656);
    font-weight: 400;
    padding: 1px 0 20px;
  }
  
  @media (max-width: 991px) {
    .example-container {
      max-width: 100%;
    }
  }
  
  .example-content {
    display: flex;
    flex-direction: column;
    font-size: 25px;
    line-height: 28px;
    padding: 0 55px 0 15px;
  }
  
  @media (max-width: 991px) {
    .example-content {
      max-width: 100%;
      padding-right: 20px;
    }
  }
  
  .decimal-representation {
    align-self: start;
    display: flex;
    gap: 10px;
    color: var(--Color-Text-text-color-primary, #303133);
    white-space: nowrap;
    line-height: 112%;
    padding: 0 1px;
  }
  
  @media (max-width: 991px) {
    .decimal-representation {
      white-space: initial;
    }
  }
  
  .decimal-label {
    font-family: Inter, sans-serif;
    flex-grow: 1;
    flex-basis: auto;
    margin: auto 0;
  }
  
  .decimal-image {
    aspect-ratio: 1.37;
    object-fit: auto;
    object-position: center;
    width: 56px;
  }
  
  .binary-representation {
    font-family: Inter, sans-serif;
    margin-top: 20px;
  }
  
  @media (max-width: 991px) {
    .binary-representation {
      max-width: 100%;
    }
  }
  
  .binary-highlight {
    color: rgba(196, 86, 86, 1);
  }
  
  .binary-text {
    color: rgba(48, 49, 51, 1);
  }
  
  .exponent-label {
    align-self: end;
    margin: 54px 55px 0 0;
    font: 18px/156% Inter, sans-serif;
  }
  
  @media (max-width: 991px) {
    .exponent-label {
      margin: 40px 10px 0 0;
    }
  }
  </style>