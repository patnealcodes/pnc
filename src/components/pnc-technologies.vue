<template>
  <section class="pnc-section pnc-technologies">
    <div class="pnc-section__container">
      <h1>PNC Technologies</h1>
      {{msg}}
    </div>
  </section>
</template>

<script>
export default {
  name: 'PNCTechnologies',
  data () {
    return {
      msg: `Technologies`
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    @import '../styles/global';
    
</style>
