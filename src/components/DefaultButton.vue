<template>
  <button>Заказать</button>
</template>

<script>
export default {

};
</script>

<style lang="scss" scoped>
button {
  width: 225px;
  height: 58px;
  border-radius: 8px;
  background-color: $darkish-pink;
  font-family: "Montserrat";
  font-size: 20px;
  font-weight: 600;
  font-stretch: normal;
  font-style: normal;
  line-height: normal;
  letter-spacing: normal;
  color: #ffffff;
  border: none;
  &:hover {
    cursor: pointer;
    background-color: $focus_button;
  }
}
</style>
