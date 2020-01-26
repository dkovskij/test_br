<template>
  <div class="cases-wrap">
    <div class="content">
      <h3>Кейсы</h3>
      <div class="list-wrap">
        <case-item
          v-for="item in cases"
          :key="item.id"
          :case-item="item"
          class="case-item-wrap"
        />
      </div>
    </div>
  </div>
</template>

<script>
import CaseItem from './CaseItem.vue';

export default {
  components: {
    CaseItem,
  },
  data() {
    return {
      cases: [],
    }
  },
  created() {
    fetch('/json/cases.json').then(r => r.json()).then((res) => {
      setTimeout(() => {
        this.cases = res.items;
      }, 500);
    });
  },
};
</script>

<style lang="scss" scoped>
.cases-wrap {
  height: 616px;
  background-color: $pale-grey;
}
.list-wrap {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-column-gap: 55px;
  margin-top: 30px;
}
.content {
  padding: 75px 100px;
  margin: 0 auto;
  width: 1148px;
}
h3 {
  font-size: 30px;
  font-weight: bold;
  font-stretch: normal;
  font-style: normal;
  line-height: normal;
  letter-spacing: normal;
  color: $dark-blue-grey;
}
.case-item-wrap {
  position: relative;
  width: 352px;
  border-radius: 10px;
  box-shadow: 0 2px 14px 0 rgba(15, 33, 53, 0.11);
  background-color: #ffffff;
}
@media screen and (max-width: 1365px) {
  .content {
    width: 782px;
  }
  .case-item-wrap {
    width: 250px;
  }
  .list-wrap {
  grid-column-gap: 25px;
}
}
</style>
