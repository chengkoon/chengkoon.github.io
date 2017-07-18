<template>
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
</template>

<script>

export default {
  name: 'main-content',
  components: {
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
