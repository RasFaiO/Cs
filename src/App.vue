<template>
  <v-app>
    <v-navigation-drawer :mini-variant="miniVariant" :clipped="clipped" v-model="drawer" app class="yellow">
      <v-list class="yellow black--text">
        <v-list-tile v-for="(item, i) in items" :key="i" @click="">
          <v-list-tile-action>
            <v-icon>{{item.icon}}</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title>{{item.title}}</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>
    <v-toolbar app :clipped-left="clipped" class="red white--text">
      <v-toolbar-side-icon @click.stop="drawer = !drawer" class="white--text"> </v-toolbar-side-icon>
      <v-btn icon @click.stop="miniVariant = !miniVariant" class="white--text">
        <v-icon v-html="miniVariant ? 'chevron_right' : 'chevron_left'"></v-icon>
      </v-btn>
      <v-btn icon @click.stop="clipped = !clipped" class="white--text">
        <v-icon>web</v-icon>
      </v-btn>
      <v-toolbar-title v-text="title"></v-toolbar-title>
      <v-spacer></v-spacer>
    </v-toolbar>
    <v-content>
      <router-view/>
    </v-content>
    <v-footer fixed tile class="indigo lighten-1 white--text text-xs-center">
      <v-card flat >
        <v-card-text>
          <v-btn v-for="icono in icons" :key="icon" icon class="mx-3 white--text">
            <v-icon size="24px">{{ icon }}</v-icon>
          </v-btn>
          <menu-icon>facebook-box</menu-icon>
        </v-card-text>
        <v-card-text class="white--text pt-0">
           
        </v-card-text>
        <v-card-text class="white--text">
          &copy;<strong>Cotrasangil</strong> - 2018
        </v-card-text>
      </v-card>
    </v-footer>
  </v-app>
</template>
<script>
export default {
  data () {
    return {
      clipped: true,
      drawer: true,
      fixed: false,
      items: [
        { icon: 'home', title: 'Principal' },
        { icon: 'receipt', title: 'Tiquetes Online' },
        { icon: 'local_shipping', title: 'Servicios' },
        { icon: 'business', title: 'Oficinas' },
        { icon: 'local_library', title: 'Corporativo' },
        { icon: 'contact_phone', title: 'Contactanos' }
      ],
      icons: [
        'fab fa-facebook', 'fab fa-twitter', 'fab fa-google-plus', 'fab fa-linkedin', 'fab fa-instagram'
      ],
      miniVariant: false,
      right: true,
      title: 'Cotrasangil'
    }
  },
  name: 'App'
}
</script>
