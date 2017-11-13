<template>
  <section class="pnc-header">
    <div class="pnc-header__container">
      <h1 class="pnc-header-text"><span class="pnc-header-text__sub">I'm Patrick Neal.</span> <span class="pnc-header-text__sub">I code things.</span></h1>
      <a class="pnc-button pnc-button--resume" href="http://resume.patrickneal.codes">
        <i class="fa fa-download"></i>
        <span>Resume</span>
      </a>
    </div>
  </section>
</template>

<script>
  export default { name: 'PNCHeader' }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  @import '../styles/global';

  .pnc-header {
    background-color: $black;
    background-image: url('../assets/header-background.jpg');
    background-position: bottom;
    background-size: cover;
    color: white;
    padding: 1em;

    @media screen and (min-width: 590px) {
      padding: 3em;
    }    
  }

  .pnc-header__container {
    align-items: center;
    display: flex;
    flex-direction: column;
    justify-content: space-between;

    @media screen and (min-width: 590px) {
      flex-direction: row;
    }
  }

  .pnc-header-text {
    margin: 0 0 1em;

    @media screen and (min-width: 590px) {
      margin: 0;
    }
  }

  .pnc-header-text__sub {
    display: block;
  }
</style>
