<template>
  <div>
    <div class="mdl-layout mdl-js-layout mdl-layout--fixed-header">
      <header class="mdl-layout__header app-menu">
        <div class="mdl-layout__header-row">
          <span class="mdl-layout-title">{{ title }}</span>
          <div class="mdl-layout-spacer"></div>
        </div>
      </header>

      <div id="menu" class="mdl-layout__drawer">
        <span class="mdl-layout-title">MENU</span>
        <nav class="mdl-navigation">
          <router-link class="mdl-navigation__link" to="/" v-on:click="closeMenu($event)">Home</router-link>
          <router-link class="mdl-navigation__link" to="/about" v-on:click="closeMenu($event)">Sobre</router-link>
        </nav>
      </div>

      <div class="container app-container">
        <router-view></router-view>
      </div>
    </div>
  </div>
</template>

<script scoped>
  export default {
    name: 'app',
    data() {
      return {
        title: 'Alimentação Escolar '
      }
    },
    methods: {
      closeMenu(event) {
        if (event) event.preventDefault();
        
        jQuery("#menu").removeClass("is-visible");
      }


    }
  }
</script>

<style>
</style>
