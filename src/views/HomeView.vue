<script setup></script>

<template>
  <main>
    <div class="heart">
      <span></span>
      <span></span>
      <span></span>
      <span></span>
      <span></span>
      <span></span>
      <span></span>
      <span></span>
      <span></span>
    </div>
  </main>
</template>
<style lang="scss" scoped>
* {
  margin: 0;
  padding: 0;
}
main {
  margin: 0; /* 设置页面外边距为0 */
  height: 100vh; /* 设置高度为视口高度 */
  display: flex; /* 使用弹性盒子布局 */
  align-items: center; /* 垂直居中 */
  justify-content: center; /* 水平居中 */
  background: radial-gradient(
    circle at center,
    #ff7e5f 0%,
    #feb47b 50%,
    #a9eeff 100%
  ); /* 设置背景为径向渐变 */
}
.heart {
  width: 280px; /* 设置心形容器宽度 */
  height: 220px; /* 设置心形容器高度 */
  display: flex; /* 使用弹性盒子布局 */
  justify-content: space-between; /* 项目之间平均分布 */
}

.heart span {
  --c: plum; /* 定义变量--c为plum */
  --h: 50%; /* 定义变量--h为50% */
  --t: 25%; /* 定义变量--t为25% */
  background-color: var(--c); /* 使用变量--c设置背景颜色 */
  width: 20px; /* 设置宽度为20px */
  border-radius: 10px; /* 设置圆角半径为10px */
  position: relative; /* 相对定位 */
  height: var(--h); /* 使用变量--h设置高度 */
  top: var(--t); /* 使用变量--t设置顶部偏移 */
  animation: beating 1s infinite; /* 应用名为beating的动画，持续时间1秒，无限循环 */
}

.heart span:nth-child(1),
.heart span:nth-child(9) {
  --c: lightcoral; /* 定义变量--c为lightcoral */
  --h: 60px; /* 定义变量--h为60px */
  --t: 44px; /* 定义变量--t为44px */
}

.heart span:nth-child(2),
.heart span:nth-child(8) {
  --c: lightskyblue; /* 定义变量--c为lightskyblue */
  --h: 120px; /* 定义变量--h为120px */
  --t: 12px; /* 定义变量--t为12px */
}

.heart span:nth-child(3),
.heart span:nth-child(7) {
  --c: lightgreen; /* 定义变量--c为lightgreen */
  --h: 160px; /* 定义变量--h为160px */
  --t: 0; /* 定义变量--t为0 */
}

.heart span:nth-child(4),
.heart span:nth-child(6) {
  --c: gold; /* 定义变量--c为gold */
  --h: 180px; /* 定义变量--h为180px */
  --t: 16px; /* 定义变量--t为16px */
}

.heart span:nth-child(5) {
  --c: plum; /* 定义变量--c为plum */
  --h: 188px; /* 定义变量--h为188px */
  --t: 32px; /* 定义变量--t为32px */
}

@keyframes beating {
  0%,
  30% {
    height: var(--h);
    top: var(--t);
    background-color: var(--c);
    filter: blur(0);
  }
  60%,
  70% {
    height: 50%;
    top: 25%;
    background-color: plum;
    filter: blur(5px);
  }
}
</style>
