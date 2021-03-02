<template>
  <div class="Logo">
    <div class="center">
      <Outer class="outer"/>
      <Inner class="inner"/>
      <Diagonal class="diagonal"/>
    </div>
  </div>
</template>
<style>
.center {
  display: inline;
  position: absolute;
  z-index: -1;
  top: 100px;
  left: 50%;
  animation: appear 1s;
}

.center > svg {
  position: relative;
  left: -50%;
}

.center .outer {
  animation: rotate-reverse 1s;
}

.center .inner {
  bottom: 164px;
  animation: rotate 1s;
}

.center .diagonal {
  bottom: 360px;
  left: -30%;
  animation: rotate 1s;
}

@keyframes rotate {
  from {
    transform: rotate(0deg);
  }
  to {
    transform: rotate(360deg);
  }
}

@keyframes rotate-reverse {
  from {
    transform: rotate(0deg);
  }
  to {
    transform: rotate(-360deg);
  }
}

@keyframes appear {
  0% {
    opacity: 0;
  }
}
</style>