<template>
  <div class="footer-menu show">
			<ul class="menu-items">
        <li @click="addHashToLocation('work')" class="menu-item menu-work" data-link="work">
          work
        </li>
        <li @click="addHashToLocation('about')" class="menu-item menu-about" data-link="about">
          about
        </li>
        <li @click="addHashToLocation('history')" class="menu-item menu-history" data-link="history">
          history
        </li>
        <li class="menu-item menu-download">
          <a class="btn" href="/2024_CV.pdf" download>
            Download CV
          </a>
        </li>
      </ul>
	</div>
</template>

<script>
  export default {
    data(){
      return{
        target:this.$route.hash
      }
    },
    async mounted(){
    },
    methods:{
      addHashToLocation(params) {
        history.pushState(
          {},
          null,
          this.$route.path + '#'  + encodeURIComponent(params)
        )
      }
    }
  }
</script>

<style lang="css" scoped>
  .footer-menu.show{
    opacity: 1;
  }
  .footer-menu {
    z-index: 100;
    padding: 0;
    margin: 0;
    position: fixed;
    bottom: 15vh;
    width: 100%;
    text-align: center;
    opacity: 0;
    transition: .4s all ease-in-out;
  }
  .footer-menu .menu-items{
    padding:0;
    margin:0;
  }
  .footer-menu .menu-item{
    display: inline-block;
    cursor: pointer;
    color: white;
    text-transform: uppercase;
    letter-spacing: 0.2vw;
    text-indent: 0.2vw;
    font-size: 1vw;
    opacity: .5;
    padding-right: 4vw;
    padding-left: 4vw;
    user-select: none;
  }
  .menu-item.menu-download{
    opacity:1;
  }
  @media only screen and (max-width: 801px){
    .footer-menu {
        bottom: 5vh;
    }
    .footer-menu .menu-item {
      font-size: 3vw;
      padding-left: 3vw;
      padding-right: 3vw;
    }
    .footer-menu .menu-item:last-child{
        padding:0;
    }
    .footer-menu .menu-item .btn{
        padding:.75rem 1rem;
    }
  }
</style>
