<template>
  <div id="app">
    <div class="glitch">
    </div>
  </div>
</template>

<script>

export default {
  name: 'app',
  components: {
  }
}
</script>

<style lang="less">
body {
  padding: 0;
  margin: 0;
}
#app {
  padding: 0;
  .glitch {
    position: relative;
    width: 100%;
    height: 100vh;
    background: url(assets/211278.jpg) center/cover no-repeat;
    &:before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: url(assets/211278.jpg) center/cover no-repeat;
      // opacity: .5;
      mix-blend-mode: hard-light;
      animation: animate .2s infinite; 
    }
    &:hover:before {
      
    }

    @keyframes animate {
      0% {
        background-position: 0 0;
        filter: hue-rotate(0deg);
      }
      10% {
        background-position: 4px 0;
      }
      20% {
        background-position: -4px 0;
      }
      30% {
        background-position: 12px 0;
      }
      40% {
        background-position: -16px 0;
      }
      50% {
        background-position: -24px 0;
      }
      60% {
        background-position: -52px 0;
      }
      70% {
        background-position: 0 22px;
      }
      80% {
        background-position: -40px -10px;
      }
      100% {
        background-position: 0 0;
        filter: hue-rotate(360deg);

      }
    }
  }
}
</style>
