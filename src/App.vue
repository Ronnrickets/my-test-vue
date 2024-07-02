<template>
  <v-app>
    <v-app-bar
    app
    dark
    dense
    color="primary"
    >
      <v-app-bar-nav-icon @click="navDrawer = !navDrawer">

      </v-app-bar-nav-icon>
    </v-app-bar>
    
    <v-navigation-drawer app v-model="navDrawer">
      <v-list>
        <v-list-item v-for="(item, i) in navList" :key="i" :to="item.to">

          <v-list-item-icon>
              <v-icon>{{ item.icon }}</v-icon>
            </v-list-item-icon>
          <v-list-item-title>{{ item.title }}</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-main>
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>

export default {
  // name: 'App',

  data: () => ({
    navDrawer:false,
    navList:[
      {title: 'Home', icon: 'mdi-home', to:'/'},
      {title: 'About', icon: 'mdi-information', to:'/about'},
    ],
  }),
};
</script>
