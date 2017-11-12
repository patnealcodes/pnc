<template>
  <section class="pnc-section pnc-about">
      <div class="pnc-section__container">
        <h1>PNC About</h1>
        {{msg}}
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
    
</style>
