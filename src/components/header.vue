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
  background-color: $dark-blue-grey;
  height: 100px;
  display: flex;
  align-content: center;
}

.content {
  width: 1266px;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 50px;
  height: 100%;
}
ul {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  list-style: none;
  column-gap: 54px;
}
.menu {
  align-self: center;
  height: 100%;
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
  display: block;
  height: 100px;
  line-height: 100px;
  text-align: center;
  &:active {
    color: $darkish-pink;
  }
  &:hover {
    border-bottom: 8px solid $darkish-pink;
    box-sizing: border-box;
  }
}
</style>
