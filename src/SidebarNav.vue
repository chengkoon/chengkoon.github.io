<template>
  <nav role="select" id="sidebar-nav" class="menu sidebar">
    <div class="fixed desktop-navbar">
      <div class="top-section">
        <div class="profile-image">
          <img src="http://i.imgur.com/QWVYWVC.png">
        </div>
        <h3 class="profile-title">Ann Cheng Koon (CKK)</h3>
        <p class="profile-description">Web Developer</p>
      </div>
      <div class="links">
        <p class="menu-label">
        </p>
        <ul class="menu-list">
          <li :class="{'activeTab': isAboutActive, 'testTab': highlightTab}"><a @click="goTo('about')"><i class="fa fa-pencil"></i>Profile</a></li>
          <li :class="{'activeTab': isProjectsActive}"><a @click="goTo('projects')"><i class="fa fa-paperclip"></i>Projects</a></li>
          <li :class="{'activeTab': isContactActive}"><a @click="goTo('contact')"><i class="fa fa-link"></i>Contact Me</a></li>
        </ul>
      </div>
    </div>
    <div class="mobile-navbar">
      <div class="mobile-profile-image">
        <img src="http://i.imgur.com/QWVYWVC.png">
      </div>
      <div class="mobile-links">
        <ul class="mobile-menu-list">
          <li><a @click="goTo('about')">Profile</a></li>
          <li><a @click="goTo('projects')">Projects</a></li>
          <li><a @click="goTo('contact')">Contact</a></li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script>
import { EventBus } from './event-bus.js'

export default {
  name: 'sidebar-nav',
  props: ['activeTab'],
  data () {
    return {
      highlightTab: false
    }
  },
  methods: {
    goTo (location) {
      EventBus.$emit('scrollTo', location)
    }
  },
  computed: {
    isAboutActive () {
      return this.activeTab === 1
    },
    isProjectsActive () {
      return this.activeTab === 2
    },
    isContactActive () {
      return this.activeTab === 3
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
.activeTab {
  background-color: rgb(73, 84, 97);
}
.testTab {
  background-color: black !important;
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
nav[role="select"] > div.mobile-navbar {
  display:none;
}
@media screen and (max-width: 802px) {
  div.desktop-navbar {
    text-align: center;
  }
}
@media screen and (max-width: 769px) {
  nav[role="select"] > div.desktop-navbar {
    display: none;
  }
  nav[role="select"] > div.mobile-navbar {
    display: flex;
    position: fixed;
    background-color: #5f6d7e;
    width: 100%;
    height: 10%;
    justify-content: space-around;
  }
  div.mobile-profile-image {
    width: 65px;
    height: 65px;
    border: 4px solid white;
    border-radius: 75px;
    overflow: hidden;
    margin: 0;
    padding: 0;
    margin-top: 5px;
    font-size: 100%;
    vertical-align: baseline;
  }
  div.mobile-links {
    display: flex;
    align-items: center;
    width: 60%;
  }
  ul.mobile-menu-list {
    width: 100%;
    display: flex;
    justify-content: space-between;
  }
  ul.mobile-menu-list li {
    display: inline;
    vertical-align: middle;
  }
  ul.mobile-menu-list li a {
    color: white;
    font-size: 18px;
  }
  /*ul.mobile-menu-list li a:hover {
    background-color: #495461;
  }*/
}

</style>
