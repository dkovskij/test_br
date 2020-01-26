<template>
  <div class="description-wrap">
    <div class="content">
      <div class="the-best">
        <h1>
          Мы – лучшая компания в Мире
        </h1>
        <div class="desc">
          Предоставляем любые услуги в любом бизнесе в день обращения
        </div>
        <div class="button-wrap">
          <default-button />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import DefaultButton from '@/components/DefaultButton.vue';

export default {
  components: {
    DefaultButton,
  },
};
</script>

<style lang="scss" scoped>
.description-wrap {
  background-image: url('../assets/wpapers-ru-white-and-blue@3x.png');
  background: {
    size: 100%;
    repeat: no-repeat;
    position: center;
  };
}
.content {
  padding: 100px 0;
}
.the-best {
  h1 {
    font-size: 42px;
    font-weight: bold;
    font-stretch: normal;
    font-style: normal;
    line-height: normal;
    letter-spacing: normal;
    color: $dark-blue-grey;
    text-align: center;
  }
  .desc {
    font-size: 28px;
    font-weight: normal;
    font-stretch: normal;
    font-style: normal;
    line-height: normal;
    letter-spacing: normal;
    text-align: center;
    color: $dark-blue-grey;
    margin-top: 33px;
  }
  .button-wrap {
    margin-top: 30px;
    text-align: center;
  }
}
@media screen and (max-width: 1365px) {
  .the-best {
    padding: 0 145px;
  }
}
</style>
