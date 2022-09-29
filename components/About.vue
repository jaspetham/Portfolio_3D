<template>
  <div id="about" class="about page hide">
    <SectionTitle :title="'about'" :subTitles="['Myself','Get to know me']"/>
    <div class="list list-content">
      <div class="divider"></div>
      <div class="info">
        <div class="bio">
          <p>
            Hello, I'm Jasper Tham, a front end developer. I am born and raised in Sabah, been there until i went overseas to Singapore and studied my diploma & degree in Singapore at June of 2017 and finished my studies in August of 2021.
          </p>
          <p class="mt-3 md:mt-6">
            During the studies, most of the projects and course is on mobile application. I do not quite enjoy making mobile application and felt lost.
            But then one day almost at the end of the studies, one of my friend introduced me to website and found out that i enjoy making the website and since then
            I never stop working on improving myself.
          </p>
          <p class="mt-3 md:mt-6">Below is my current skillset.</p>
          <div class="grid grid-cols-2 gap-3 mt-5 md:mt-10">
            <div>
              <p>Frontend Skills</p>
              <ul class="mt-5 list-disc list-inside">
                <li class="skills-item">VueJS/NuxtJS</li>
                <li class="skills-item">Bootstrap</li>
                <li class="skills-item">Tailwind CSS</li>
                <li class="skills-item">ReactJS</li>
              </ul>
            </div>
            <div>
              <p>Others Skills</p>
              <ul class="mt-5 list-disc list-inside">
                <li class="skills-item">ThreeJS (3D)</li>
                <li class="skills-item">Javascript</li>
                <li class="skills-item">Jquery</li>
                <li class="skills-item">Postman API</li>
                <li class="skills-item">Basic SQL</li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import SectionTitle from './SectionTitle.vue';
  export default {
    components: { SectionTitle }
}
</script>

<style lang="css" scoped>
  .info .bio{
    margin-inline: auto;
    width: 90vw;
    font-size: 1.4vw;
    padding-bottom:10vw;
  }
  .info .bio p{
    opacity:.9;
  }
  .skills-item{
    font-size:1vw;
    font-weight:400;
    margin-bottom:1rem;
  }

  @media only screen and (max-width: 801px){
    .info .bio {
      font-size: 2.5vh;
    }
    .skills-item{
      font-size:2vh;
    }
    .divider{
      margin-top:5vh;
      margin-bottom:0;
    }
  }
</style>
