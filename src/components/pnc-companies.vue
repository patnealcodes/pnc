<template>
  <section class="pnc-section pnc-companies">
    <div class="pnc-section__container">
      <h1>Companies I've Worked With</h1>
      <ul class="pnc-companies-list">
        <li class="pnc-company" v-for="company in companies" :key="company.name">
          <img :src="imgSrc(company)" :alt="company.name">
        </li>
      </ul>
    </div>
  </section>
</template>

<script>
const imagePath = require.context('../assets', true)

export default {
  name: 'PNCCompanies',
  methods: {
    imgSrc: function (company) {
      return `${imagePath(`./${company.filename}`, true)}`
    }
  },
  data () {
    return {
      companies: [
        {
          filename: 'fidelity.png',
          name: 'Fidelity Investments'
        },
        {
          filename: 'mare.png',
          name: 'Massachusetts Adoption Resource Exchange'
        },
        {
          filename: 'ascena.png',
          name: 'Ascena Retail'
        },
        {
          filename: 'eyemed.png',
          name: 'Eyemed Visioncare'
        },
        {
          filename: 'bnc.png',
          name: 'Barnes &amp; Noble - College'
        },
        {
          filename: 'webster.png',
          name: 'Webster Bank'
        },
        {
          filename: 'bertuccis.png',
          name: 'Bertucci\'s Italian Restaurant'
        },
        {
          filename: 'ram.png',
          name: 'Dodge Ram'
        },
        {
          filename: 'sunglasshut.png',
          name: 'Sunglass Hut'
        },
        {
          filename: 'lebronjames.png',
          name: 'Lebron James'
        }
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    @import '../styles/global';
    
    .pnc-companies-list {
      align-items: center;
      display: flex;
      justify-content: space-around;
      flex-wrap: wrap;
    }

    .pnc-company {
      margin: 1em 1em 0;

      img {
        max-width: 120px;
      }
    }
</style>
