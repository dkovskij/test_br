<template>
  <footer>
    <div class="content">
      <div class="description">
        <div class="text">
          Следите за нашей компанией, подпишитесь на рассылку, мы не будем навязчивыми
        </div>
        <div class="footnote">
          Новости выходят один раз в неделю в самом лучшем формате
        </div>
      </div>
      <div class="form">
        <div class="input">
          <input type="text" placeholder="Ваш e-mail" v-model="userEmail">
        </div>
        <div class="checkbox">
          <input type="checkbox" id="my-checkbox" v-model="isChecked">
          <label for="my-checkbox"></label>
          <span>Согласен с <a href="#">условиями</a> сервиса</span>
        </div>
        <div class="buttons">
          <div class="subscribe">
            <button>Подписаться</button>
          </div>
          <div class="cancel">
            <button>Не хочу</button>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  data() {
    return {
      userEmail: '',
      isChecked: false,
    };
  },
};
</script>

<style lang="scss" scoped>
a {
  color: $darkish-pink;
}
.content {
  width: 1148px;
  margin: 0 auto;
  padding: 75px 100px;
  display: grid;
  grid-template-columns: 1fr 1fr;
  column-gap: 119px;
}
.text {
  font-family: "Montserrat";
  font-size: 22px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.45;
  letter-spacing: normal;
  color: $dark-blue-grey;
}
.footnote {
  font-family: "Montserrat";
  font-size: 14px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.43;
  letter-spacing: normal;
  color: $bluish-grey;
  margin-top: 65px;
}
.input {
  input {
    width: calc(100% - 22px);
    padding-left: 20px;
    height: 44px;
    border-radius: 8px;
    border: solid 1px $bluish-grey;
    background-color: #ffffff;
    font-family: "Montserrat";
    font-size: 16px;
    font-weight: normal;
    font-stretch: normal;
    font-style: normal;
    line-height: normal;
    letter-spacing: normal;
    color: $dark-blue-grey;
    outline: none;
    &:focus {
      border: solid 1px $darkish-pink;
    }
    &::placeholder {
      color: $bluish-grey;
    }
  }
}
.checkbox {
  position: relative;
  margin-top: 27px;
  input[type="checkbox"]:checked,
  input[type="checkbox"]:not(:checked) {
      position: absolute;
      left: -9999px;
  }
  input[type="checkbox"]:checked + label,
  input[type="checkbox"]:not(:checked) + label {
      display: inline-block;
      position: relative;
      padding-left: 20px;
      padding-top: 20px;
      line-height: 20px;
      cursor: pointer;
  }
  input[type="checkbox"]:checked + label:before,
  input[type="checkbox"]:not(:checked) + label:before {
    content: "";
    position: absolute;
    left: 0px;
    top: 3px;
    width: 19px;
    height: 19px;
    border: 1px solid $bluish-grey;
    border-radius: 3px;
}
  input[type="checkbox"]:checked + label:hover:before,
  input[type="checkbox"]:not(:checked) + label:hover:before {
    border: 1px solid $darkish-pink;
  }

input[type="checkbox"]:checked + label:before {
  background-color: $darkish-pink;
  border: 1px solid $darkish-pink;
}
input[type="checkbox"]:not(:checked) + label:before {
  background-color: #ffffff;
}
input[type="checkbox"]:checked + label:after,
input[type="checkbox"]:not(:checked) + label:after {
    content: "";
    position: absolute;
    -webkit-transition: all 0.2s ease;
    -moz-transition: all 0.2s ease;
    -o-transition: all 0.2s ease;
    transition: all 0.2s ease;
}

input[type="checkbox"]:checked + label:after {
  border-left: 3px solid #ffffff;
  border-bottom: 3px solid #ffffff;
}

input[type="checkbox"]:checked + label:after,
input[type="checkbox"]:not(:checked) + label:after {
    left: 4px;
    top: 8px;
    width: 10px;
    height: 5px;
    border-radius: 1px;
    -webkit-transform: rotate(-45deg);
    -moz-transform: rotate(-45deg);
    -o-transform: rotate(-45deg);
    -ms-transform: rotate(-45deg);
    transform: rotate(-45deg);
}
input[type="checkbox"]:not(:checked) + label:after {
    opacity: 0;
}

input[type="checkbox"]:checked + label:after {
    opacity: 1;
}
span {
  font-family: "Montserrat";
  font-size: 16px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: normal;
  letter-spacing: normal;
  color: $dark-blue-grey;
  margin-left: 15px;
}
}
.buttons {
  margin-top: 32px;
  display: flex;
}
.subscribe {
  button {
    cursor: pointer;
    width: 183px;
    height: 44px;
    border: none;
    outline: none;
    border-radius: 8px;
    background-color: $darkish-pink;
    font-family: "Montserrat";
    font-size: 16px;
    font-weight: 600;
    font-stretch: normal;
    font-style: normal;
    line-height: normal;
    letter-spacing: normal;
    color: #ffffff;
    &:hover {
      background-color: $focus-button;
    }
  }
}
.cancel {
  margin-left: 17px;
  button {
    cursor: pointer;
    width: 137px;
    height: 44px;
    background-color: #fff;
    outline: none;
    border-radius: 8px;
    border: solid 1px $darkish-pink;
    font-family: "Montserrat";
    font-size: 16px;
    font-weight: 600;
    font-stretch: normal;
    font-style: normal;
    line-height: normal;
    letter-spacing: normal;
    color: $darkish-pink;
    &:hover {
      border: solid 1px $focus-button;
      background-color: $focus-button;
      color: #ffffff;
    }
  }
}
@media screen and (max-width: 1365px) {
  .content {
    width: 782px;
  }
}
</style>
