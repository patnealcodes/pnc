<template>
  <section class="pnc-section pnc-about">
    <div class="pnc-section__container">
      <div class="pnc-about-content">
        <h1>Freelance</h1>
        <p><b>Note:</b> I am <span class="not--sadface">not</span> currently seeking freelance positions <i class="fa fa-frown-o"></i></p>
        <p>However, I would be a fool to blindly reject an opportunity! Feel free to <a class="pnc-link" href="mailot:apparently@patrickneal.codes">reach out</a> if you have an interesting idea <i class="fa fa-smile-o"></i></p>
      </div>
    </div>
  </section>
</template>

<script>
  export default { name: 'PNCFreelance' }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    @import '../styles/global';

    .not--sadface {
      color: #b11c19;
      text-decoration: underline;
    }
</style>
