<template>
  <div id="app">
    <HeaderComponent />

    <main>
      <MainComponent />
    </main>
  </div>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue'
import MainComponent from './components/MainComponent.vue'

export default {
  name: 'App',
  components: {
    HeaderComponent,
    MainComponent
  }
}
</script>

<style lang="scss">
@import '@/assets/style/variables.scss';

// reset
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

#app {
  background-color: $primary_color;
}
</style>
