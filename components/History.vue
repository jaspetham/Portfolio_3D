<template>
  <div id="history" class="history page hide">
    <SectionTitle :title="'history'" :subTitles="['Educations', 'Work Experience']"/>
    <div class="list list-content">
      <div class="divider"></div>
      <div class="wrapper">
        <div class="grid md:grid-cols-2 grid-cols-1 gap-6">
          <div class="info-content">
            <h1 class="info-title mb-5">Educations</h1>
            <ul class="list-unstyled">
              <li v-for="(graduation,index) in graduations" :key="index">
                <div class="flex gap-4">
                  <div class="relative content-icon">
                    <div class="icon">
                      <font-awesome-icon :icon="['fas','graduation-cap']"/>
                    </div>
                  </div>
                  <div class="content">
                    <div class="year">{{graduation.year}}</div>
                    <h1 class="info-title">
                      {{graduation.type}}
                    </h1>
                    <span class="info-subtitle">{{graduation.school}}</span>
                    <p class="info-text">{{graduation.info}}</p>
                  </div>
                </div>
              </li>
            </ul>
          </div>
          <div class="info-content">
            <h1 class="info-title mb-5">Work Experience</h1>
            <ul class="list-unstyled">
              <li v-for="(work,index) in works" :key="index">
                <div class="flex gap-4">
                  <div class="relative content-icon">
                    <div class="icon">
                      <font-awesome-icon :icon="['fas','suitcase']"/>
                    </div>
                  </div>
                  <div class="content">
                    <div class="year">{{work.year}}</div>
                    <h1 class="info-title">
                      {{work.type}}
                    </h1>
                    <span class="info-subtitle">{{work.school}}</span>
                    <p class="info-text">{{work.info}}</p>
                  </div>
                </div>
              </li>
            </ul>
          </div>
        </div>
        <div class="divider"></div>
        <div class="flex justify-center">
          <a class="btn" href="~/assets/Resume_Eng.pdf" download>
            Download CV
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    data(){
      return{
        graduations:[
          {
            year:'July 2017 - August 2019',
            type: 'BACHELOR DEGREE',
            school: 'COVENTRY UNIVERSITY, Singapore',
            info: 'Bachelor Of Science in Computer Science, Graduated with Upper Second Class Division'
          },
          {
            year:'April 2016 - April 2017',
            type: 'Diploma',
            school: 'PSB Academy, Singapore',
            info: 'Diploma in Infocomm &amp; Technology, Pass with merit'
          }
        ],
        works:[
          {
            year:'June 2022 - July 2022',
            type: 'Front End Developer(Contract Staff)',
            school: 'My AOne Learning Sdn. Bhd, Malaysia',
            info: 'Responsible for the conversion of a design element into a working website, Accurately translate user and business needs into functional frontend code & develop and maintain web-based frontend application in Javascript/VueJS'
          },
          {
            year:'June 2021 - June 2022',
            type: 'Web Developer',
            school: 'Unicom Interactive Digital, Malaysia',
            info: 'In charge of the frontend projects, assigned to create multiple responsive websites based on the design given from scratch to functional websites. Use Laravel framework as based and HTML, CSS, Bootstrap for frontend.'
          },
          {
            year:'November 2020 - June 2021',
            type: 'Junior Web Developer',
            school: 'Coreka Co, Malaysia',
            info: 'Responsible for creating the front end of several real life website. The website is built in opencart platform which is PHP based. I also have the responsibility of doing the backend of the project including using ajax,jquery validation and getting/saving data into phpmyadmin sql.'
          },
          {
            year:'November 2019 - June 2021',
            type: 'Apprentice Web Developer',
            school: 'Phisoft, Malaysia',
            info: 'Have a hands on creating a website with microweber platform and uses bootstrap 4.'
          }
        ],
      }
    }
  }
</script>

<style lang="css" scoped>
  div.wrapper{
    margin-inline: auto;
    width: 90vw;
    padding-bottom:10vw;
  }
  .info-content .year{
    font-size:0.8vw;
    background:var(--clr-main);
    color:white;
    width: fit-content;
    padding: 0.25rem 0.5rem;
    border-radius:25px;
    margin-bottom:1rem;
  }
  .info-content :is(.info-title,.icon), .btn{
    font-size:1.4vw;
  }
  .info-content .info-subtitle{
    font-size: 1.2vw;
    opacity: .8;
    position: relative;
  }
  .info-content .info-text{
    font-size:1.2vw;
    text-transform: none;
    margin-top:1.5rem;
  }
  .icon{
    padding:.75rem;
    text-align: center;
    z-index: 1;
    border-radius: 50%;
    color: #fff;
    background-color: var(--clr-main);
    display:flex;
    align-content: center;
    justify-content: center;
    position: relative;
  }
  ul > li{
    text-transform: uppercase;
    position: relative;
    margin-bottom:2.5rem;
  }
  ul > li:last-child{
    margin-bottom:0;
  }

  .content-icon::after{
    content: "";
    position: absolute;
    top:0;
    width:3px;
    border-radius:15px;
    height:100%;
    background:var(--clr-main);
    left: 50%;
    transform: translateX(-50%);
  }

  @media only screen and (max-width: 801px){
    .info-content :is(.info-title,.icon), .btn {
      font-size: 2.5vh;
    }
    .info-content .info-subtitle{
      font-size: 2vh;
      display:block;
    }
    .info-content .info-subtitle::before{
      display:none;
    }
    .info-content .info-text{
      font-size:2vh;
      margin-top:.75rem;
    }
    .info-content .year{
      font-size:1.75vh;
      margin-bottom:.75rem;
    }
    .divider{
      margin-top:5vh;
      margin-bottom:0;
    }
  }
</style>
