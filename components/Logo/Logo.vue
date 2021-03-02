<template>
  <div class="Logo">
    <div class="center relative">
      <Outer class="outer absolute inset-x-0 mx-auto" />
      <Inner class="inner absolute inset-x-0 mx-auto" />
      <Diagonal class="diagonal absolute inset-x-0 mx-auto" />
    </div>
  </div>
</template>
<style>
.center {
  animation: appear 1s;
}

.center .outer {
  animation: rotate-reverse 1s;
}

.center .inner {
  animation: rotate 1s;
}

.center .diagonal {
  animation: rotate 1s;
  top: -30px;
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