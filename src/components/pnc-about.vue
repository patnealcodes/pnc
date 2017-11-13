<template>
  <section class="pnc-section pnc-about">
      <div class="pnc-section__container">
        <div class="pnc-about-content">
          <h1>About Me</h1>
          <p>Hello! I'm Patrick Neal - a full stack web-app developer out of Boston, MA. My primary passion lies in coding intricate yet intuitive user experiences, and working to ensure the best experience for the end user.</p>
        </div>
        <div class="pnc-about-image">
          <img src="../assets/me.jpg" alt="Me!"> 
        </div>
  </div>
  </section>
</template>

<script>
export default {
  name: 'PNCAbout',
  data () {
    return {
      msg: `About Section`
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    @import '../styles/global';

    .pnc-section__container {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    
    .pnc-about-image {
      display: none;
      margin: 0 0 0 2em;
      z-index: 3;

      img {
        width: 14em;
        border: .5em solid white;
        border-radius: 50%;
      }

      @media screen and (min-width: 590px) {
        display: block;
      }
    }
</style>
