<template>
  <div class="background-fx"> 
    <img src="../assets/shape-01.svg" class="shape-01"> 
    <img src="../assets/shape-02.svg" class="shape-02"> 
    <img src="../assets/shape-03.svg" class="shape-03"> 
    <img src="../assets/shape-04.svg" class="shape-04"> 
    <img src="../assets/shape-05.svg" class="shape-05"> 
    <img src="../assets/shape-06.svg" class="shape-06"> 
    <img src="../assets/shape-07.svg" class="shape-07"> 
    <img src="../assets/shape-08.svg" class="shape-08"> 
    <img src="../assets/shape-09.svg" class="shape-09"> 
    <!-- <img src="../assets/shape-10.svg" class="shape-10">  -->
    <img src="../assets/shape-11.svg" class="shape-11"> 
    </div>
</template>
<script>
export default {
  
}
</script>
<style scoped>
.background-fx {
    height: auto;
    overflow: hidden;
    opacity: 1;
    z-index: -1
  }

  .shape-01 {
    position: absolute;
    top: 11%;
    right: 42%;
    -webkit-animation: animationFramesTwo 13s linear infinite;
    animation: animationFramesTwo 13s linear infinite
  }

  .shape-02 {
    position: absolute;
    top: 27%;
    left: 17%;
    -webkit-animation: animationFramesFour 25s linear infinite alternate;
    animation: animationFramesFour 25s linear infinite alternate
  }

  .shape-03 {
    position: absolute;
    top: 30%;
    left: 50%;
    -webkit-animation: animationFramesThree 35s linear infinite alternate;
    animation: animationFramesThree 35s linear infinite alternate
  }

  .shape-04 {
    position: absolute;
    top: 40%;
    right: 23%;
    -webkit-animation: animationFramesFour 20s linear infinite alternate;
    animation: animationFramesFour 20s linear infinite alternate
  }

  .shape-05 {
    position: absolute;
    bottom: 62%;
    right: 28%;
    -webkit-animation: animationFramesOne 15s linear infinite;
    animation: animationFramesOne 15s linear infinite
  }

  .shape-06 {
    position: absolute;
    bottom: 73%;
    left: 38%;
    -webkit-animation: animationFramesFour 20s linear infinite alternate;
    animation: animationFramesFour 20s linear infinite alternate
  }

  .shape-07 {
    position: absolute;
    left: 14%;
    bottom: 54%;
    -webkit-animation: animationFramesOne 17s linear infinite;
    animation: animationFramesOne 17s linear infinite
  }

  .shape-08 {
    position: absolute;
    left: 14%;
    top: 60%;
    -webkit-animation: animationFramesOne 20s linear infinite alternate;
    animation: animationFramesOne 20s linear infinite alternate
  }

  .shape-09 {
    position: absolute;
    top: 22%;
    left: 41%;
    -webkit-animation: animationFramesOne 15s linear infinite;
    animation: animationFramesOne 15s linear infinite
  }

  .shape-10 {
    position: absolute;
    top: 8%;
    right: 6%;
    -webkit-animation: animationFramesOne 15s linear infinite;
    animation: animationFramesOne 15s linear infinite
  }

  .shape-11 {
    position: absolute;
    top: 10%;
    right: 8%;
    -webkit-animation: animationFramesOne 12s linear infinite;
    animation: animationFramesOne 12s linear infinite
  }

  @keyframes animationFramesOne {
    0% {
      transform: translate(0) rotate(0deg)
    }

    20% {
      transform: translate(73px, -1px) rotate(36deg)
    }

    40% {
      transform: translate(141px, 72px) rotate(72deg)
    }

    60% {
      transform: translate(83px, 122px) rotate(108deg)
    }

    80% {
      transform: translate(-40px, 72px) rotate(144deg)
    }

    to {
      transform: translate(0) rotate(0deg)
    }
  }

  @-webkit-keyframes animationFramesOne {
    0% {
      -webkit-transform: translate(0) rotate(0deg)
    }

    20% {
      -webkit-transform: translate(73px, -1px) rotate(36deg)
    }

    40% {
      -webkit-transform: translate(141px, 72px) rotate(72deg)
    }

    60% {
      -webkit-transform: translate(83px, 122px) rotate(108deg)
    }

    80% {
      -webkit-transform: translate(-40px, 72px) rotate(144deg)
    }

    to {
      -webkit-transform: translate(0) rotate(0deg)
    }
  }

  @keyframes animationFramesTwo {
    0% {
      transform: translate(0) rotate(0deg) scale(1)
    }

    20% {
      transform: translate(73px, -1px) rotate(36deg) scale(.9)
    }

    40% {
      transform: translate(141px, 72px) rotate(72deg) scale(1)
    }

    60% {
      transform: translate(83px, 122px) rotate(108deg) scale(1.2)
    }

    80% {
      transform: translate(-40px, 72px) rotate(144deg) scale(1.1)
    }

    to {
      transform: translate(0) rotate(0deg) scale(1)
    }
  }

  @-webkit-keyframes animationFramesTwo {
    0% {
      -webkit-transform: translate(0) rotate(0deg) scale(1)
    }

    20% {
      -webkit-transform: translate(73px, -1px) rotate(36deg) scale(.9)
    }

    40% {
      -webkit-transform: translate(141px, 72px) rotate(72deg) scale(1)
    }

    60% {
      -webkit-transform: translate(83px, 122px) rotate(108deg) scale(1.2)
    }

    80% {
      -webkit-transform: translate(-40px, 72px) rotate(144deg) scale(1.1)
    }

    to {
      -webkit-transform: translate(0) rotate(0deg) scale(1)
    }
  }

  @keyframes animationFramesThree {
    0% {
      transform: translate(165px, -179px)
    }

    to {
      transform: translate(-346px, 617px)
    }
  }

  @-webkit-keyframes animationFramesThree {
    0% {
      -webkit-transform: translate(165px, -179px)
    }

    to {
      -webkit-transform: translate(-346px, 617px)
    }
  }

  @keyframes animationFramesFour {
    0% {
      transform: translate(-300px, 151px) rotate(0deg)
    }

    to {
      transform: translate(251px, -200px) rotate(180deg)
    }
  }

  @-webkit-keyframes animationFramesFour {
    0% {
      -webkit-transform: translate(-300px, 151px) rotate(0deg)
    }

    to {
      -webkit-transform: translate(251px, -200px) rotate(180deg)
    }
  }
</style>