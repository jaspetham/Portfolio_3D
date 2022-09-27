<template>
  <div>
    <div class="top-bar bar"></div>
    <Canvas/>
    <Home/>
    <Work/>
    <MobileMenu/>
    <Header/>
    <Footer/>
    <div class="bottom-bar bar"></div>
  </div>
</template>

<script>
import Canvas from '../components/Canvas.vue';
import Home from '../components/Home.vue';
import Footer from '../components/Footer.vue';
import Header from '../components/Header.vue';
import MobileMenu from '../components/MobileMenu.vue';
import AOS from 'aos'
import 'aos/dist/aos.css'

export default {
  name: "IndexPage",
  components: { Canvas, Home, Footer, Header, MobileMenu },
  mounted() {
    AOS.init({ })
  }
}
</script>
<style lang="css" scoped>
  .top-bar.bar,.bottom-bar.bar {
    height: 10vh;
  }
  .bar.hide{
    height:0vh;
    min-height: 0;
  }
  .top-bar {
    width: 100vw;
    height: 50vh;
    background: black;
    position: fixed;
    z-index: 1000;
    top: 0;
    transition: .3s ease-in-out;
  }
  .bottom-bar {
    width: 100vw;
    height: 50vh;
    background: black;
    position: fixed;
    z-index: 1000;
    bottom: 0;
    text-align: center;
    transition: .3s ease-in-out;
  }
  .page {
    width: 100vw;
    height:100%;
    position: absolute;
    transform: translate3d(0,20%,0);
    top: 0px;
    left: 0px;
    z-index: 0;
    background: none;
    opacity: 0;
    padding-bottom: 10vw;
    transition: .8s ease-in-out;
  }
  .page.show {
    z-index: 100;
    opacity: 1;
    transform: translate3d(0,0,0);
  }
  .page.hide {
    display: none;
  }
  @media only screen and (max-width: 801px){
    .bottom-bar.bar, .top-bar.bar {
      height: 0;
      min-height: 0;
    }
  }
</style>
