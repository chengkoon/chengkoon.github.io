<template>
  <div id="app">
    <div class="columns is-gapless is-desktop">
      <sidebar-nav :activeTab="activeTab">First column</sidebar-nav>
      <main-content></main-content>
    </div>
  </div>
</template>

<script>
import { EventBus } from './event-bus.js'
import SidebarNav from './SidebarNav.vue'
import MainContent from './MainContent.vue'

export default {
  name: 'app',
  components: {
    'sidebar-nav': SidebarNav,
    'main-content': MainContent
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
