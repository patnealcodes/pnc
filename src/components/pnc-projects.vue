<template>
  <section class="pnc-section pnc-projects">
    <div class="pnc-section__container">
      <h1>Notable Projects</h1>
      <ul class="pnc-projects-list">
        <li class="pnc-project" v-for="project in projects" :key="project.name">
          <img class="pnc-project-image" :src="imgSrc(project)" :alt="imgAlt(project)">
          <div class="pnc-project-overlay" :style="{'background-color': `#${project.colorHex}`}"></div>
          <div class="pnc-project-content">
            <span class="pnc-project-name" :style="{'background-color': `#${project.colorHex}`}">{{ project.name }}</span>
            <i class="pnc-project-expand fa fa-expand"></i>
            <span class="pnc-project-description">{{ project.description }}</span>
          </div>
        </li>
      </ul>
    </div>
  </section>
</template>

<script>
const imagePath = require.context('../assets', true)

export default {
  name: 'PNCProjects',
  methods: {
    imgSrc: function (project) {
      return `${imagePath(`./${project.filename}`, true)}`
    },
    imgAlt: function (project) {
      return `${project.name} ${project.description}`
    }
  },
  data () {
    return {
      projects: [
        {
          filename: 'schneider-wall.jpg',
          name: 'Schnieder Electric',
          description: 'Interactive Wall',
          colorHex: '169d50'
        },
        {
          filename: 'voya-claims.jpg',
          name: 'Voya',
          description: 'Claim Center',
          colorHex: 'd75426'
        },
        {
          filename: 'maurices.jpg',
          name: 'Maurices',
          description: 'eCommerce Site',
          colorHex: '5cb7b3'
        }
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  @import '../styles/global';
  
  .pnc-projects-list {
    display: flex;
    justify-content: space-around;
    flex-wrap: wrap;
  }

  .pnc-project {
    box-shadow:
      0 0 .125em 0 rgba(0,0,0,.125),
      0 .125em .125em 0 rgba(0,0,0,.25);
    border-radius: .25em;
    cursor: pointer;
    overflow: hidden;
    margin: 2em 0 0;
    max-width: 200px;
    position: relative;

    img {
      display: block;
    }
  }

  .pnc-project-image {
    height: 100%;
  }

  .pnc-project-overlay {
    bottom: 0;
    display: block;
    left: 0;
    right: 0;
    opacity: 0;
    position: absolute;
    transition: .3s all ease-in-out;
    top: 0;

    .pnc-project:hover & {
      opacity: .75;
    }
  }

  .pnc-project-content {
    align-items: center;
    bottom: 0;
    color: white;
    display: flex;
    flex-direction: column;
    font-weight: 500;
    justify-content: space-around;
    left: 0;
    right: 0;
    position: absolute;
    text-shadow: .05em .05em .05em rgba(0,0,0,.5);
    transition: .3s all ease-in-out;
    top: 0;
  }

  .pnc-project-name {
    padding: .25em .5em;
    border-radius: .25em;
  }

  .pnc-project-expand {
    opacity: 0;
    font-size: 3em;
    transition: .3s all;

    .pnc-project:hover & {
      opacity: 1;
    }
  }

  .pnc-project-description {
    opacity: 0;
    transition: .3s all;

    .pnc-project:hover & {
      opacity: 1;
    }
  }
</style>
