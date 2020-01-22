<template>
  <header>
    <div class="content">
      <div class="logo">
        <img src="../assets/logo.svg" alt="logo">
      </div>
      <div class="menu">
        <nav>
          <ul>
            <li
              v-for="(item, index) in navMenu"
              :key="'nav' + index"
              class="menu-item"
            >
              <a :href="item.url">{{ item.label }}</a>
            </li>
          </ul>
        </nav>
      </div>
    </div>
  </header>
</template>

<script>

export default {
  data() {
    return {
      navMenu: [
        { label: 'О компании', url: '#' },
        { label: 'Кейсы', url: '#' },
        { label: 'Контакты', url: '#' },
      ]
    };
  },
};
</script>

<style lang="scss" scoped>
header {
  background-color: $header_background;
  height: 100px;
}

.content {
  max-width: 1366px;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
  align-content: center;
}
ul {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  list-style: none;
  column-gap: 54px;
}

.menu-item a {
  font-family: "Montserrat";
  font-size: 16px;
  font-weight: bold;
  font-stretch: normal;
  font-style: normal;
  line-height: normal;
  letter-spacing: normal;
  color: #ffffff;
}
</style>
