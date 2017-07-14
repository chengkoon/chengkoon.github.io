<template>
  <!-- <div id="main-content" class="main">
    <div class="content-wrapper"> -->

      <section class="hero">
        <div id="about" class="hero-body">
          <h4 class="opener">From one of my favourite stand-up comedians ⇩</h4><br>
          <div class="about-image">
              <img src="http://i.imgur.com/bKK5B2l.jpg" alt="about me">
          </div>
          <p>Having recently graduated from National University of Singapore (NUS) with a Bachelor's in Arts (History), I took the unconventional step in enrolling
          in the 12-weeks <strong>Web Development Immersive</strong> course at <strong>General Assembly</strong>. I believe in the role of technology in levelling society
          and I am excited in taking part in this possibility.
          <br><br>Thanks for your interest in my work, scroll down for more and I look forward to meeting new friends over a cup of tea/coffee/beer/any non-soda drinks!</p>
          <br><br><br><hr>
        </div>
      </section>
      <!-- <projects></projects> -->
      <!-- <section class="hero">
        <div id="projects" class="hero-body columns">
          <div class="column is-4">
            <div class="project-item1">
              <img src="http://i.imgur.com/zejeln5.png" alt="">
              <div class="project-hover">
                <div class="inside">
                  <strong>2-Player Memory Game</strong>
                  <p>A two-player game built with Javascript and jQuery for funky animations and effects. <br>Click <a href="https://github.com/chengkoon/2P-memorygame/">here</a> to see the code and the demo.</p>
                </div>
              </div>
            </div>
          </div>
          <div class="column is-4">
            <div class="project-item2">
              <img src="http://i.imgur.com/FyYjmut.png" alt="">
              <div class="project-hover">
                <div class="inside">
                  <strong>Tapau - Community Food Delivery App</strong>
                  <p>2nd project in the course, used Nodejs for the project's backend. Full authentication services and dealt with the complex time object</p>
                  Click <a href="https://github.com/chengkoon/project2">here</a> for the demo and code.
                </div>
              </div>
            </div>
          </div>
          <div class="column is-4">
            <div class="project-item3">
              <img src="http://i.imgur.com/qzU9DdJ.png" alt="">
              <div class="project-hover">
                <div class="inside">
                  <strong>Tikam! Unique bidding system</strong>
                  <p>Sponsors provide items up for bid and gain free advertisement while users stand a chance to win cheap products</p>
                  Click <a href="https://github.com/chengkoon/project4-improved">here</a> for the demo and code.
                </div>
              </div>
            </div>
          </div>
        </div>
      </section> -->
    <!-- </div>
  </div> -->
</template>

<script>
// import Projects from './Projects.vue'

export default {
  name: 'main-content',
  components: {
    // 'projects': Projects
  },
  data () {
    return {
    }
  },
  methods: {
  }
}
</script>

<style>
h4.opener {
  font-size: 16px;
  font-weight: 600;
}
/*.main {
  height: 100%;
}
.content-wrapper {
  padding: 0 80px;
}*/
.about-image {
  overflow: hidden;
  border: 4px solid #dddddd;
  margin-bottom: 40px;
}
.about-image img {
  width: 100%;
  display: block;
}
#about p {
  text-align: justify;
  text-justify: inter-word;
}
.big-box {
  border: 2px solid black;
  height: 300px;
}
</style>
