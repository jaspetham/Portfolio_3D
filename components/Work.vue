<template>
  <div id="work" class="work page hide">
    <SectionTitle :title="'work'" :subTitles="['Personal','Projects','Experiments']"/>
    <div class="list">
      <a class="list-item"
        target="_blank"
        data-aos-easing="ease-in-out"
        data-aos="fade-up"
        data-aos-offset="0"
        data-aos-duration="1000"
        data-aos-delay="0"
        v-for="project in projects"
        :key="project.id"
        :href="project.url"
      >
        <div v-for="index in 8" :key="index" class="hover-point"></div>
        <div class="box-contents">
          <img class="box-img" :src="project.imgSrc" alt="">
          <div class="box-details">
            <div class="box-subtitle">{{project.type}}</div>
            <div class="box-title">{{project.name}}</div>
          </div>
        </div>
      </a>
    </div>
  </div>
</template>

<script>
import SectionTitle from './SectionTitle.vue';
import project1 from '~/assets/img/work1-min.jpg';
import project2 from '~/assets/img/work2-min.jpg';
import project3 from '~/assets/img/work3-min.jpg';
import project4 from '~/assets/img/work4-min.jpg';
import project5 from '~/assets/img/work5-min.jpg';
import project6 from '~/assets/img/work6-min.jpg';
import project7 from '~/assets/img/work7-min.jpg';
import project8 from '~/assets/img/work8-min.jpg';
import project9 from '~/assets/img/work9-min.jpg';
import project10 from '~/assets/img/work10-min.jpg';
import project11 from '~/assets/img/work11-min.jpg';
import project12 from '~/assets/img/work12-min.jpg';
import projectBiteFamily from '~/assets/img/bite-family-min.png';
import projectZestProduction from '~/assets/img/zest-production-min.png';
import projectOrganicBall from '~/assets/img/organic-ball-min.png';

  export default {
  components: { SectionTitle },
  data(){
    return{
      projects:[
        {
          url:'https://jaspetham.github.io/Super-Nova/',
          type:'Personal Project',
          name:'NuxtJS, Super Nova',
          imgSrc:project1
        },
        {
          url:'https://jasper-keynabalu.netlify.app',
          type:'Personal Project | Facebook Group',
          name:'NuxtJS, Keyboard Anonymous',
          imgSrc:project2
        },
        {
          url:'https://jaspetham.github.io/space-solution/',
          type:'Personal Project | Frontend Challenge',
          name:'React, Space Solution',
          imgSrc:project3
        },
        {
          url:'https://jasper-zest-production.netlify.app/',
          type:'Client Project |',
          name:'React, Zest Production',
          imgSrc:projectZestProduction
        },
        {
          url:'https://jasper-bite-family.netlify.app/',
          type:'Client Project | On Hold',
          name:'React, Bite Family',
          imgSrc:projectBiteFamily
        },
        {
          url:'https://jasper-threejs-portfolio-v1.netlify.app/',
          type:'Personal Project | Portfolio',
          name:'ThreeJS, Portfolio Test',
          imgSrc:project12
        },
        {
          url:'https://jasper-threejs-organic-ball.netlify.app/',
          type:'Personal Project | 3D Expriments',
          name:'ThreeJS, Organic Ball',
          imgSrc:projectOrganicBall
        },
        {
          url:'https://jasper-threejs-galaxy-generator.netlify.app/',
          type:'Personal Project | 3D Expriments',
          name:'ThreeJS, Galaxy Demo',
          imgSrc:project10
        },
        {
          url:'https://jaspetham.github.io/Wave-Demo/',
          type:'Personal Project | 3D Expriments',
          name:'ThreeJS, Wave Demo',
          imgSrc:project11
        },
        {
          url:'https://jasper-threejs-video-explode.netlify.app',
          type:'Personal Project | 3D Expriments',
          name:'ThreeJS, Video Explode Particle',
          imgSrc:project8
        },
        {
          url:'https://jasper-threejs-noise-beauty.netlify.app',
          type:'Personal Project | 3D Expriments',
          name:'ThreeJS, Noise Beauty',
          imgSrc:project6
        },
        {
          url:'https://jaspetham.github.io/Icosahedron/',
          type:'Personal Project | 3D Expriments',
          name:'ThreeJS, Icosahedron',
          imgSrc:project7
        },
        {
          url:'https://jasper-threejs-particles-map.netlify.app',
          type:'Personal Project | 3D Expriments',
          name:'ThreeJS, Particles Map',
          imgSrc:project4
        },
        {
          url:'https://jasper-threejs-explode-particle.netlify.app/',
          type:'Personal Project | 3D Expriments',
          name:'ThreeJS, Explode Particle',
          imgSrc:project9
        },
        {
          url:'https://jasper-threejs-pixel-distortion.netlify.app',
          type:'Personal Project | 3D Expriments',
          name:'ThreeJS, Pixel Distortions',
          imgSrc:project5
        },
      ]
    }
  }
}
</script>

<style lang="css" scoped>
  .box-contents {
    position: absolute;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    box-shadow: 0 0 50px rgba(var(--box-shadow));
    transition: .5s ease;
  }
  .box-contents > .box-img{
    object-fit: cover;
    width: 100%;
    height:100%;
  }
  .box-contents .box-details{
    position: absolute;
    left:0;
    bottom:-1px;
    background:rgba(0,0,0,.8);
    width:100%;
    padding:1rem;
    opacity:0;
    visibility:hidden;
    transition: all .5s ease-in;
    text-transform: uppercase;
    padding: 2vw;
    padding-top: 1vw;
  }
  .box-details > * {
    color:white;
    z-index:10;
  }
  .box-details .box-subtitle{
      color: grey;
      text-transform: uppercase;
      margin-bottom: 0.5vw;
      transition: .1s all;
      font-size: 1vw;
      font-family: var(--ff-secondary);
  }
  .box-details .box-title{
    color: white;
    text-transform: uppercase;
    letter-spacing: 1px;
    transition: .1s all;
    font-size: 1.4vw;
    font-family: var(--ff-secondary);
  }
  .list-item:hover .box-details{
    opacity:1;
    visibility: visible;
  }
  .hover-point {
    position: absolute;
    z-index: 2;
    width: calc(100% / 3);
    height: calc(100% / 3);
  }
  .hover-point:nth-child(1) {
    top: 0;
    left: 0;
  }
  .hover-point:nth-child(2) {
    top: 0;
    left: calc(100% / 3);
  }
  .hover-point:nth-child(3) {
    top: 0;
    right: 0;
  }
  .hover-point:nth-child(4) {
    top: calc(100% / 3);
    left: 0;
  }
  .hover-point:nth-child(5) {
    top: calc(100% / 3);
    right: 0;
  }
  .hover-point:nth-child(6) {
    bottom: 0;
    left: 0;
  }
  .hover-point:nth-child(7) {
    bottom: 0;
    left: calc(100% / 3);
  }
  .hover-point:nth-child(8) {
    bottom: 0;
    right: 0;
  }
  .hover-point:nth-child(1):hover ~ .box-contents {
    box-shadow: 15px 15px 50px rgba(var(--box-shadow));
    transform-origin: right top;
    transform: perspective(5000px) rotateX(10deg) rotateY(-10deg) rotateZ(2deg);
  }
  .hover-point:nth-child(2):hover ~ .box-contents {
    box-shadow: 0 15px 50px rgba(var(--box-shadow));
    transform-origin: center top;
    transform: perspective(5000px) rotateX(10deg);
  }
  .hover-point:nth-child(3):hover ~ .box-contents {
    box-shadow: -15px 15px 50px rgba(var(--box-shadow));
    transform-origin: left top;
    transform: perspective(5000px) rotateX(10deg) rotateY(10deg) rotateZ(-2deg);
  }
  .hover-point:nth-child(4):hover ~ .box-contents {
    box-shadow: 15px 5px 50px rgba(var(--box-shadow));
    transform-origin: left center;
    transform: perspective(5000px) rotateY(-10deg);
  }
  .hover-point:nth-child(5):hover ~ .box-contents {
    box-shadow: -15px 5px 50px rgba(var(--box-shadow));
    transform-origin: right center;
    transform: perspective(5000px) rotateY(10deg);
  }
  .hover-point:nth-child(6):hover ~ .box-contents {
    box-shadow: 15px -15px 50px rgba(var(--box-shadow));
    transform-origin: right bottom;
    transform: perspective(5000px) rotateX(-10deg) rotateY(-10deg) rotateZ(-2deg);
  }
  .hover-point:nth-child(7):hover ~ .box-contents {
    box-shadow: 0 -15px 50px rgba(var(--box-shadow));
    transform-origin: center bottom;
    transform: perspective(5000px) rotateX(-10deg);
  }
  .hover-point:nth-child(8):hover ~ .box-contents {
    box-shadow: -15px -15px 50px rgba(var(--box-shadow));
    transform-origin: left bottom;
    transform: perspective(5000px) rotateX(-10deg) rotateY(10deg) rotateZ(2deg);
  }
</style>
