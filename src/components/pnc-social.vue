<template>
  <section class="pnc-social">
    <div class="pnc-social__container">
      <h1>PNC Social</h1>
      {{msg}}
    </div>
  </section>
</template>

<script>
export default {
  name: 'PNCSocial',
  data () {
    return {
      msg: `Social Section`
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    @import '../styles/global';
    
    .pnc-social {
      background: $black;
      color: white;
    }
</style>
