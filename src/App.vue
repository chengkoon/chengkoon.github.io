<template>
  <div id="app">
    <div class="columns is-gapless is-desktop">
      <sidebar-nav>First column</sidebar-nav>
      <main-content></main-content>
    </div>
  </div>
</template>

<script>
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

    }
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
