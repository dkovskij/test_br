<template>
  <div id="app">
    <Header />
    <description />
    <cases />
    <div class="footer-wrap">
      <footer-component />
    </div>
  </div>
</template>

<script>
import Header from '@/components/Header.vue';
import Description from '@/components/Description.vue';
import Cases from '@/components/Cases.vue';
import FooterComponent from '@/components/FooterComponent.vue';

export default {
  components: {
    Header,
    Description,
    Cases,
    FooterComponent,
  },
};
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css?family=Montserrat:400,500,600,700&display=swap&subset=cyrillic');

* {
  margin: 0;
  padding: 0;
}
a {
  text-decoration: none;
}
#app {
  font-family: 'Montserrat', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
