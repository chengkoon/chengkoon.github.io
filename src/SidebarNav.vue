<template>
  <aside id="sidebar-nav" class="menu sidebar column is-3">
    <div class="fixed">
      <div class="top-section">
        <div class="profile-image">
          <img src="./assets/img/profilepic.png">
        </div>
        <h3 class="profile-title">Ann Cheng Koon (CK)</h3>
        <p class="profile-description">Web Developer</p>
      </div>
      <div class="links">
        <p class="menu-label">
        </p>
        <ul class="menu-list">
          <li><a href="#about"><i class="fa fa-pencil"></i>Profile</a></li>
          <li><a href="#projects"><i class="fa fa-paperclip"></i>Projects</a></li>
          <li><a href="#contact"><i class="fa fa-link"></i>Contact Me</a></li>
        </ul>
      </div>
    </div>
  </aside>
</template>

<script>
export default {
  name: 'sidebar-nav',
  data () {
    return {

    }
  }
}
</script>

<style>
.sidebar {
  background-color: #5f6d7e;
  /*height: 100%;*/
  color: white;
}
.fixed {
  position: fixed;
  width: inherit;
}
.top-section {
  /*padding: 40px;*/
  display: flex;
  flex-direction: column;
  align-items: center;
  /*text-align: center;*/
  /*width: inherit;*/
  /*margin: 0 auto;*/
}
div.profile-image {
  width: 150px;
  height: 150px;
  border: 4px solid white;
  border-radius: 75px;
  overflow: hidden;
  margin: 0;
  padding: 0;
  margin-top: 60px;
  margin-bottom: 20px;
  font-size: 100%;
  vertical-align: baseline;
}
img {
  border: 0;
}
.menu-list a {
  color: white;
  padding: 15px 40px;
  text-align: left;
  line-height: 24px;
}
.menu-list li a i {
  margin-right: 15px;
  font-size: 24px;
}
h3.profile-title {
  margin-bottom: 5px;
  color: white;
  font-size: 18px;
  font-weight: 700;
}

/*@font-face {
  font-family: 'robotobold';
  src: url("./assets/fonts/Roboto-Bold-webfont.eot");
  src: url("./assets/fonts/Roboto-Bold-webfont.eot?#iefix") format("embedded-opentype");
  src: url("./assets/fonts/Roboto-Bold-webfont.woff") format("woff");
  src: url("./assets/fonts/Roboto-Bold-webfont.ttf") format("truetype");
  src: url("./assets/fonts/Roboto-Bold-webfont.svg#robotobold") format("svg");
  font-weight: normal;
  font-style: normal;
}*/
</style>
