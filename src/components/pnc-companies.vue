<template>
  <section class="pnc-section pnc-companies">
    <div class="pnc-section__container">
      <h1>PNC Companies</h1>
      {{msg}}
    </div>
  </section>
</template>

<script>
export default {
  name: 'PNCCompanies',
  data () {
    return {
      msg: `Companies`
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    @import '../styles/global';
    
</style>
