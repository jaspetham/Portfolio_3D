<template>
  <div id="menu" class="menu">
		<ul class="menu-items">
      <li class="menu-item menu-home" data-link="home">home</li>
      <li class="menu-item menu-work" data-link="work">work</li>
      <li class="menu-item menu-about" data-link="about">about</li>
      <li class="menu-item menu-history" data-link="history">history</li>
      <li class="menu-item menu-education" data-link="education">education</li>
    </ul>
	</div>
</template>

<script>
  export default {

  }
</script>

<style lang="css" scoped>
  .menu.show{
    opacity: 1;
    z-index: 1000;
    display: block;
  }
  .menu {
    opacity: 0;
    width: 100vw;
    height: 100%;
    left: 50%;
    top: 50%;
    position: fixed;
    transform: translate(-50%,-50%);
    padding: 0;
    margin: 0;
    transition: 1s all;
    z-index: 0;
    background: #000;
  }
  .menu .menu-items {
    left: 50%;
    top: 50%;
    position: absolute;
    transform: translate(-50%,-50%);
    padding: 0;
    margin: 0;
    margin-top: 0vw;
  }
  .menu .menu-item{
    cursor: pointer;
    list-style: none;
    opacity: .5;
    text-align: center;
    font-size: 9vw;
    line-height: 10vh;
    text-transform: uppercase;
    color: white;
  }
</style>
