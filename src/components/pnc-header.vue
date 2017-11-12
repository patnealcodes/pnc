<template>
  <section class="pnc-header">
    <div class="pnc-header__container">
      <h1>PNC Header</h1>
      {{msg}}
    </div>
  </section>
</template>

<script>
export default {
  name: 'PNCHeader',
  data () {
    return {
      msg: `Welcome to Patrick Neal's Portfolio!`
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    @import '../styles/global';

    .pnc-header {
      background: $black;
      color: white;
    }
</style>
