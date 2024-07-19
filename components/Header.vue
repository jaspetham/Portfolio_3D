<template>
  <div id="header" class="header">
    <div class="header-menu">
      <ul class="menu-items">
        <li class="menu-item menu-home" data-link="home">home</li>
        <li class="menu-item menu-work" data-link="work">| work</li>
        <li class="menu-item menu-about" data-link="about">| about</li>
        <li class="menu-item menu-history" data-link="history">| history</li>
        <li class="menu-item ml-3 menu-download">
          <a class="btn" href="/2024_CV.pdf" download> Download CV </a>
        </li>
      </ul>
    </div>
    <div class="menu-button">
      <span></span>
      <span></span>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="css" scoped>
.header.show {
  opacity: 1;
  visibility: visible;
  z-index: 1000;
  top: 0;
}

.header {
  opacity: 0;
  position: fixed;
  width: 100vw;
  height: 12vh;
  top: -5vh;
  left: 0;
  padding: 0;
  margin: 0;
  transition: 1s all ease-in-out;
  z-index: 1000;
  visibility: hidden;
}

.header-menu {
  padding: 0;
  margin: 0;
  z-index: 0;
  position: absolute;
  right: 5vw;
  top: 5vh;
}

.header-menu .menu-item {
  display: inline-block;
  cursor: pointer;
  color: white;
  text-transform: uppercase;
  letter-spacing: 0.2vw;
  font-size: 0.9vw;
  opacity: 0.5;
  padding-right: 6.5px;
}

.menu-item.menu-download{
    opacity:1;
}
.menu-download .btn{
    padding:1rem 1.5rem;
}

.menu-button,
.menu-button span {
  display: inline-block;
  transition: all 0.3s;
  box-sizing: border-box;
}

.menu-button {
  width: 30px;
  height: 60px;
  position: absolute;
  top: 30px;
  right: 30px;
  cursor: pointer;
  z-index: 1000;
  display: none;
}

.menu-button span {
  position: absolute;
  left: 0;
  width: 100%;
  height: 0.2vw;
  min-height: 1px;
  background-color: #fff;
  opacity: 1;
  border-radius: 0vw;
}

.menu-button span:nth-of-type(1) {
  top: 0vw;
}

.menu-button span:nth-of-type(2) {
  top: 2vw;
}

.menu-button.active span:nth-of-type(1) {
  -webkit-transform: translateY(1vw) rotate(-45deg);
  transform: translateY(1vw) rotate(-45deg);
}

.menu-button.active span:nth-of-type(2) {
  -webkit-transform: translateY(-1vw) rotate(45deg);
  transform: translateY(-1vw) rotate(45deg);
}

@media only screen and (max-width: 801px) {
  .header-menu {
    display: none;
  }

  .menu-button {
    display: block;
    opacity: 0.5;
  }
}
</style>
