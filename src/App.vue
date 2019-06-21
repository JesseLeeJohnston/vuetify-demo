<template>
  <v-app>
    <v-toolbar app>
      <v-toolbar-title class="headline text-uppercase">
        <span>Patient</span>
        <span class="font-weight-light">EDITOR</span>
      </v-toolbar-title>
      <v-spacer></v-spacer>

    <v-toolbar-items class="hidden-sm-and-down">
      <v-btn flat to="/">
        Home
      </v-btn>
      <v-btn flat to="about">
        About
      </v-btn>
      <v-btn flat to="contact">
        Contact
      </v-btn>
    </v-toolbar-items>
      
    </v-toolbar>

    <v-content>
      
        <transition name="fade" mode="out-in">
          <router-view></router-view>
        </transition>
      
    </v-content>
  </v-app>
</template>

<script>

export default {
  name: 'App',
  data: {
  theme: {
    primary: '#3f51b5',
    secondary: '#b0bec5',
    accent: '#8c9eff',
    error: '#b71c1c'
  }

  },
  components: {
    
  },
  data () {
    return {
      //
    }
  }
}
</script>
<style lang="scss" scoped>
.fade-enter-active,
.fade-leave-active {
  transition-duration: 0.3s;
  transition-property: opacity;
  transition-timing-function: ease;
}

.fade-enter,
.fade-leave-active {
  opacity: 0
}
</style>
