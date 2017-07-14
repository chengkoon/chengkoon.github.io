<template lang="html">
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
            <!-- <input class="input is-danger" type="text" placeholder="hello@me.com" name="email"> -->
            <input class="input" type="text" placeholder="hello@me.com" name="email">
            <span class="icon is-small is-left">
              <i class="fa fa-envelope"></i>
            </span>
            <span class="icon is-small is-right">
              <!-- <i class="fa fa-warning"></i> -->
            </span>
          </p>
          <!-- <p class="help is-danger">This email is invalid</p> -->
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
</template>

<script>
export default {
  name: 'contact-form'
}
</script>

<style lang="css">
</style>
