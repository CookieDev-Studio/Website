<template>
  <v-app dark>
    <v-navigation-drawer
      v-model="drawer"
      fixed
      app
      dark
      color="drawer"
      class="drawer"
    >
      <v-list>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        >
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar
      fixed
      app
      color="nav"
      dark
      class="app-bar"
    >
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
      <v-toolbar-title v-text="title" />
      <v-spacer />
    </v-app-bar>
    <v-main>
      <nuxt />
    </v-main>
    <v-footer
      :absolute="!fixed"
      app
    >
      <div style="width: 100%; text-align: center;">
        <a href="https://github.com/CookieDev-Studio" target="_blank">
          <div class="footer-img" id="github" />
        </a> | 
        <a href="https://patreon.com/cookiedevstudio" target="_blank">
          <div class="footer-img" id="patreon" />
        </a>        
      </div>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Home',
          to: '/'
        },
        {
          icon: 'mdi-account-supervisor',
          title: 'About',
          to: '/About'
        },
        {
          icon: 'mdi-email',
          title: 'Contact',
          to: '/Contact'
        }
      ],
      title: 'Cookie Dev Studio'
    }
  }
}
</script>

<style scoped>
.drawer {
  z-index: 20;
  max-height: none !important;
}

.app-bar {
  z-index: 10;
}

.footer-img {
  width: 30px;
  height: 30px;
  display: inline-block;
  margin: auto;
}

#github {
  background-image: url('../static/octocat.jpg');
  background-size: cover;
  background-position: center;
}

#patreon {
  background-image: url('../static/Patreon_Mark_Coral.jpg');
  background-size: cover;
  background-position: center;
}
</style>