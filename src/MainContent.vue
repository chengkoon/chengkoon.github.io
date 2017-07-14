<template>
  <div id="main-content" class="main column is-9">
    <div class="content-wrapper">

      <section class="hero">
        <div id="about" class="hero-body">
          <h4>This is me in my normal state ⇩</h4>
          <div class="about-image">
              <img src="./assets/img/8.jpg" alt="about me">
          </div>
          <p>Having recently graduated from National University of Singapore (NUS) with a Bachelor's in Arts (History), I took the unconventional step in enrolling
          in the 12-weeks <strong>Web Development Immersive</strong> course at <strong>General Assembly</strong>. I believe in the role of technology in levelling society
          and I am excited in taking part in this possibility.
          <br><br>Thank you for having an interest in me and my work, please scroll down for more and I look forward to making and meeting new friends over a cup of tea/coffee/beer/any non-soda drinks!</p>
          <hr>
        </div>
      </section>

      <section class="hero">
        <div id="projects" class="hero-body columns">
          <div class="column is-3">
            <div class="project-item">
              <img src="http://i.imgur.com/zejeln5.png" alt="">
              <div class="project-hover">
                <div class="inside">
                  <h5>2-Player Memory Game</h5>
                  <p>This is a two-player game built with Javascript and jQuery in 5 days of hair-plucking. <br>Click <a href="https://github.com/chengkoon/2P-memorygame/">here</a> to see the code and the demo.</p>
                </div>
              </div>
            </div>
          </div>
          <div class="column is-3">
            <div class="project-item">
              <img src="img/2.jpg" alt="">
              <div class="project-hover">
                <div class="inside">
                  <h5>Tapau - Community Food Delivery App</h5>
                  <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam cursus</p>
                </div>
              </div>
            </div>
          </div>
          <div class="column is-3">
            <div class="project-item">
              <img src="img/3.jpg" alt="">
              <div class="project-hover">
                <div class="inside">
                  <h5><a href="#">Pellentesque porta ligula</a></h5>
                  <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam cursus.</p>
                </div>
              </div>
            </div>
          </div>
          <div class="column is-3">
            <div class="project-item">
              <img src="img/4.jpg" alt="">
              <div class="project-hover">
                <div class="inside">
                  <h5><a href="#">Pellentesque porta ligula</a></h5>
                  <p>Quisque mattis sit amet dolor eu scelerisque. Vivamus bibendum massa et nisl tempus commodo.</p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>

      <hr>

      <section class="hero">
        <div id="contact" class="hero-body">
          <form action="https://formspree.io/chengkoon@gmail.com" method="POST">
            <div class="field">
              <label class="label">Your name please</label>
              <p class="control">
                <input class="input" type="text" name="name">
              </p>
            </div>

            <div class="field">
              <label class="label">Your email?</label>
              <p class="control has-icons-left has-icons-right">
                <input class="input is-danger" type="text" placeholder="hello@me.com" name="email">
                <span class="icon is-small is-left">
                  <i class="fa fa-envelope"></i>
                </span>
                <span class="icon is-small is-right">
                  <i class="fa fa-warning"></i>
                </span>
              </p>
              <p class="help is-danger">This email is invalid</p>
            </div>

            <div class="field">
              <label class="label">Your message (if any?)</label>
              <p class="control">
                <textarea class="textarea" name="message"></textarea>
              </p>
            </div>

            <div class="field is-grouped">
              <p class="control">
                <input type="submit" class="button is-primary" value="Submit">
              </p>
              <p class="control">
                <button type="button" name="button" class="button is-info">Clear</button>
              </p>
            </div>
          </form>
        </div>
      </section>
    </div>
  </div>
</template>

<script>
export default {
  name: 'main-content',
  data () {
    return {

    }
  }
}
</script>

<style>
.main {
  height: 100%;
}
.content-wrapper {
  padding: 0 80px;
}
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
