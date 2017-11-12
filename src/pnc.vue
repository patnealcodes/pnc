<template>
  <div class="pnc-portfolio">
    <PNCHeader/>

    <div class="pnc-portfolio__sections">
      <PNCAbout/>
      <PNCTechnologies/>
      <PNCProjects/>
      <PNCCompanies/>
    </div>

    <PNCSocial/>
  </div>
</template>

<script>
import PNCHeader from './components/pnc-header'
import PNCAbout from './components/pnc-about'
import PNCTechnologies from './components/pnc-technologies'
import PNCProjects from './components/pnc-projects'
import PNCCompanies from './components/pnc-companies'
import PNCSocial from './components/pnc-social'

export default {
  name: 'pnc',
  components: {
    PNCHeader,
    PNCAbout,
    PNCTechnologies,
    PNCProjects,
    PNCCompanies,
    PNCSocial
  }
}
</script>

<!-- Global Styles -->
<style lang="scss">
  @import './styles/global';

  .pnc-portfolio {
    display: flex;
    flex-direction: column;
    min-height: 100vh;
  }

  .pnc-portfolio__sections {
    display: flex;
    flex: 1;
    flex-direction: column;
    justify-content: space-evenly;
  }
</style>
