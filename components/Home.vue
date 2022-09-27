<template>
    <div id="home" class="home page show">
      <div class="title-wrap">
        <h1 class="title">Jasper Tham</h1>
        <p class="sub-title">Front end developer</p>
      </div>
    </div>
</template>

<script>
  export default {
    mounted(){
    }
  }
</script>

<style lang="css" scoped>
  .home{
    overflow: hidden;
    height: 100%;
    padding-bottom: 0;
    pointer-events: none;
  }
  .title-wrap{
    top: 50%;
    left: 50%;
    width: 100%;
    z-index: 100;
    position: absolute;
    transform: translate(-50%, -50%);
    text-align: center;
    margin: 0;
    padding: 0;
  }
  .title{
    text-transform: uppercase;
    text-align: center;
    font-size: 5vw;
    letter-spacing: 2.6vw;
    color: var(--clr-main);
    color: hsla(var(--hsl-main), 1);
    filter: drop-shadow(0px 6px 10px var(--clr-main));
    text-indent: 2.6vw;
    opacity: 1;
    font-weight: 300;
    position: relative;
    top: 0;
    left: auto;
    transform: none;
    padding: 0;
    margin: 0;
    position: relative;
  }
  .sub-title{
    text-transform: uppercase;
    text-align: center;
    font-size: 1.5vw;
    letter-spacing: 1.75vw;
    text-indent: 1.8vw;
    top: 0;
    left: auto;
    transform: none;
    padding: 0;
    margin: 0;
    position: relative;
    color:var(--clr-main);
  }
  @media only screen and (max-width: 801px){
    .home .title {
      font-size: 8vw;
    }
    .home .sub-title {
      font-size: 2.2vw;
    }
  }
</style>
