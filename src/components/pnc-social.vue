<template>
  <section class="pnc-social">
    <div class="pnc-social__container">
      <ul class="pnc-social-list">
        <li>
          <a href="mailto:apparently@patrickneal.codes" class="pnc-social-item">
            <i class="pnc-icon--email fa fa-envelope"></i>
          </a>
        </li>
        <li v-for="item in social" :key="item.name">
          <a :href="item.url" class="pnc-social-item" :title="item.name" target="_blank">
            <i :class="faIcon(item)"></i>
          </a>
        </li>
      </ul>
    </div>
  </section>
</template>

<script>
export default {
  name: 'PNCSocial',
  methods: {
    faIcon: function (item) {
      return `pnc-icon--${item.icon} fa fa-${item.icon}`
    }
  },
  data () {
    return {
      social: [
        {
          icon: 'github',
          name: 'GitHub',
          url: 'https://github.com/patnealcodes'
        },
        {
          icon: 'linkedin',
          name: 'LinkedIn',
          url: 'https://www.linkedin.com/in/patnealcodes/'
        },
        {
          icon: 'codepen',
          name: 'CodePen',
          url: 'https://codepen.io/patnealcodes/'
        },
        {
          icon: 'twitter',
          name: 'Twitter',
          url: 'https://twitter.com/patnealcodes'
        }
      ]
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

    .pnc-social-list {
      display: flex;
      justify-content: center;
    }

    .pnc-social-item {
      color: white;
      font-size: 2em;
      padding: 0 .25em;
      transition: .3s all;
    }

    .pnc-icon {
      &--email {
        background: $email-red;
        border-radius: 0.1em;
        color: $email-gray;
        line-height: 0.75em;
        overflow: hidden;
      }

      &--twitter {
        color: $twitter;
      }

      &--linkedin {
        color: $linkedin;
      }
    }
</style>
