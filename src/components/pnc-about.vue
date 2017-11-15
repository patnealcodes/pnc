<template>
  <section class="pnc-section pnc-about">
      <div class="pnc-section__container">
        <div class="pnc-about-content">
          <h1>About Me</h1>
          <p class="pnc-about-text--primary">Hello! I'm Patrick Neal - a full stack web-app developer out of Boston, MA. My primary passion lies in coding intricate yet intuitive user experiences, and working to ensure the best experience for the end user.</p>
          <p class="pnc-about-text--secondary">I love learning new things, staying on the bleeding edge of the ever-emerging web technologies, and immersing myself in the projects I take on. I am a self-taught developer, picking it up out of curiosity, and continuing to learn out of excitement and the sheer joy of it.</p>
          <p class="pnc-about-text--tertiary">While I consider myself very well versed in web development and the surrounding technology areas - it is my opinion that one of the most important things is to stay humble, and stay hungry (for learning). You will always learn new things, you will always find better ways to do things, and you should always be able to look back and notice things you could’ve done better. The moment you stop learning is the moment you begin to deprecate yourself as a developer.</p>
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

    .pnc-about-text {
      &--secondary {
        display: none;

        @media screen and (min-width: 640px) {
          display: block;
        }
      }

      &--tertiary {
        display: none;

        @media screen and (min-width: 780px) {
          display: block;
        }
      }
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
