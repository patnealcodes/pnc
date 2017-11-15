<template>
  <section class="pnc-section pnc-technologies">
    <div class="pnc-section__container">
      <h1>Technologies</h1>
      <ul class="pnc-technologies-list">
        <li class="pnc-technology" v-for="tech in technologies" :key="tech.name">
          <i :class="techClass(tech)"></i>
          <span class="pnc-technology-text">{{tech.name}}</span>
        </li>
      </ul>
    </div>
  </section>
</template>

<script>
export default {
  name: 'PNCTechnologies',
  methods: {
    techClass: function (tech) {
      return `pnc-technology-icon ${tech.devicon}`
    }
  },
  data () {
    return {
      technologies: [
        {
          devicon: 'devicon-html5-plain colored',
          name: 'HTML 5'
        },
        {
          devicon: 'devicon-sass-plain colored',
          name: 'SASS'
        },
        {
          devicon: 'devicon-bootstrap-plain colored',
          name: 'Bootstrap'
        },
        {
          devicon: 'devicon-javascript-plain colored',
          name: 'JavaScript'
        },
        {
          devicon: 'devicon-typescript-plain colored',
          name: 'TypeScript'
        },
        {
          devicon: 'devicon-angularjs-plain colored',
          name: 'Angular'
        },
        {
          devicon: 'devicon-react-plain colored',
          name: 'React'
        },
        {
          devicon: 'devicon-backbonejs-plain colored',
          name: 'BackboneJS'
        },
        {
          devicon: 'devicon-nodejs-plain colored',
          name: 'Node'
        },
        {
          devicon: 'devicon-express-original colored',
          name: 'Express'
        },
        {
          devicon: 'devicon-mongodb-plain colored',
          name: 'MongoDB'
        },
        {
          devicon: 'devicon-babel-plain colored',
          name: 'Babel'
        },
        {
          devicon: 'devicon-webpack-plain colored',
          name: 'Webpack'
        },
        {
          devicon: 'devicon-docker-plain colored',
          name: 'Docker'
        },
        {
          devicon: 'devicon-nginx-plain colored',
          name: 'NGINX'
        }
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    @import '../styles/global';

    .pnc-technologies-list {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
    }

    .pnc-technology {
      align-items: center;
      display: flex;
      flex-direction: column;
      justify-content: center;
      padding: 1em;

      @media screen and (min-width: 590px) {
        padding: 1.75em;
      }
    }

    .pnc-technology-icon {
      font-size: 2.5em;
    }

    .pnc-technology-text {
      display: none;

      @media screen and (min-width: 590px) {
        display: block;
      }
    }
</style>
