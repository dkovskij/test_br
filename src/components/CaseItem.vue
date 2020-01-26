<template>
  <div>
    <div class="content">
      <div v-if="caseItem.img" :style="`background-image:url(${caseImg});`" class="image" />
      <div class="wrapper">
        <div class="date">
          {{ caseItem.date }}
        </div>
        <div class="title">
          {{ caseItem.title }}
        </div>
        <div v-if="!caseItem.img" class="text">
          {{ caseItem.text }}
        </div>
      </div>
      <div class="read-all">
        <span @mouseenter="iconColor = '#e43898'" @mouseleave="iconColor = '#7f8d9c'" :style="'color:' + iconColor + ';'">
          Читать полностью
        </span>
        <span @mouseenter="iconColor = '#e43898'" @mouseleave="iconColor = '#7f8d9c'">
          <icon-base :width="39" :height="12" :view-box="'0 0 39 12'" :icon-color="iconColor">
            <icon-arrow-right />
          </icon-base>
        </span>
      </div>
    </div>
  </div>
</template>

<script>
import IconBase from '@/icons/IconBase.vue';
import IconArrowRight from '@/icons/IconArrowRight.vue';

export default {
  components: {
    IconBase,
    IconArrowRight,
  },
  props: {
    caseItem: {
      type: Object,
      required: true,
    },
  },
  computed: {
    caseImg() {
      return require('../' + this.caseItem.img);
    },
  },
  data() {
    return {
      iconColor: '#7f8d9c',
    };
  },
};
</script>

<style lang="scss" scoped>
.content {
  height: 397px;
  .wrapper {
    padding: 20px 25px;
  }
}
.image {
  border-top-left-radius: 10px;
  border-top-right-radius: 10px;
  height: 163px;
  background-size: cover;
  background-position: center center;
}
.date {
  font-family: "Montserrat";
  font-size: 14px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: normal;
  letter-spacing: normal;
  color: $bluish-grey;
}
.title {
  font-family: "Montserrat";
  font-size: 16px;
  font-weight: bold;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.5;
  letter-spacing: normal;
  color: $dark-blue-grey;
  margin-top: 10px;
  cursor: pointer;
}
.text {
  font-family: "Montserrat";
  font-size: 14px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.43;
  letter-spacing: normal;
  color: $dark-blue-grey;
  margin-top: 12px;
  word-wrap: break-word;
}
.read-all {
  display: flex;
  justify-content: space-between;
  position: absolute;
  bottom: 0;
  height: 63px;
  border-top: 1px solid $pale-grey;
  padding: 0 25px;
  line-height: 63px;
  width: calc(100% - 50px);
  span {
    cursor: pointer;
    &:hover {
      color: $darkish-pink;
    }
  }
  // &::after {
  //   content: "";
  //   position: absolute;
  //   top: 50%;
  //   transform: translateY(-50%);
  //   right: 25px;
  //   width: 39px;
  //   height: 12px;
  //   background: url('../assets/arrow.svg') no-repeat;
  // }
  // &:hover:after {
  //   background: url('../assets/arrow-pink.svg') no-repeat;
  // }
}
@media screen and (max-width: 1365px) {

}
</style>
