<template>
  <div id="app">
    <div class="columns is-gapless">
      <sidebar-nav :activeTab="activeTab" class="column is-3">First column</sidebar-nav>
      <div class="column is-9 main" id="main">
        <div class="content-wrapper">
          <main-content></main-content>
          <projects></projects>
          <contact-form></contact-form>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { EventBus } from './event-bus.js'
import SidebarNav from './SidebarNav.vue'
import MainContent from './MainContent.vue'
import Projects from './Projects.vue'
import ContactForm from './ContactForm.vue'
const sr = require('scrollreveal')()

export default {
  name: 'app',
  components: {
    'sidebar-nav': SidebarNav,
    'main-content': MainContent,
    'projects': Projects,
    'contact-form': ContactForm
  },
  data () {
    return {
      scrollPosition: '',
      prevScrollPosition: '',
      activeTab: '',
      aboutPos: '',
      projectsPos: '',
      contactPos: ''
    }
  },
  methods: {
    updateScrollProp () {
      this.scrollPosition = window.scrollY
      this.aboutPos = document.getElementById('about').offsetTop
      this.projectsPos = document.getElementById('projects').offsetTop - 160
      this.contactPos = document.getElementById('contact').offsetTop - 150
      console.log('about is ', this.aboutPos)
      console.log('projects is ', this.projectsPos)
    },
    handleScroll () {
      this.scrollPosition = window.scrollY
      console.log('scroll is ', this.scrollPosition)
      if (this.scrollPosition > this.prevScrollPosition) {
        if ((this.scrollPosition >= this.aboutPos) && (this.scrollPosition < this.projectsPos)) {
          this.activeTab = 1
        }
        if ((this.scrollPosition >= this.projectsPos) && (this.scrollPosition < this.contactPos)) {
          this.activeTab = 2
          this.something = true
        }
        if (this.scrollPosition >= this.contactPos) {
          this.activeTab = 3
        }
      }
    }
  },
  created () {
    window.addEventListener('scroll', this.handleScroll)
  },
  mounted () {
    this.updateScrollProp()
    EventBus.$on('scrollTo', (location) => {
      if (location === 'about') {
        this.activeTab = 1
        window.scrollTo(0, this.aboutPos)
      } else if (location === 'projects') {
        this.activeTab = 2
        window.scrollTo(0, this.projectsPos)
      } else if (location === 'contact') {
        this.activeTab = 3
        window.scrollTo(0, this.contactPos)
      }
    })
  },
  updated () {
    sr.reveal('.project-item1', { origin: 'bottom', duration: 300, delay: 500 })
    sr.reveal('.project-item2', { origin: 'bottom', duration: 300, delay: 700 })
    sr.reveal('.project-item3', { origin: 'bottom', duration: 300, delay: 900 })
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /*text-align: center;*/
  color: #2c3e50;
}
.main {
  height: 100%;
}
.content-wrapper {
  padding: 0 80px;
}

.main-content {
  background-color: green;
}

h1, h2 {
  font-weight: normal;
}

/*ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}*/

a {
  color: #42b983;
}
</style>
