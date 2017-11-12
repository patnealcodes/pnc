<template>
  <section class="pnc-section pnc-projects">
    <div class="pnc-section__container">
      <h1>PNC Projects</h1>
      {{msg}}
    </div>
  </section>
</template>

<script>
export default {
  name: 'PNCProjects',
  data () {
    return {
      msg: `Projects`
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    @import '../styles/global';
    
</style>
