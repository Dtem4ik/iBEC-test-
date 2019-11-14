<template>
  <div class="index">
    <div class="container">
      <div class="row">
        <div class="col-xl-10 col-12">
          <div class="row">
            <div v-for="i in 8" :key="`card-${i}`" class="col-xl-6 col-12">
              <div class="index__card rounded">
                <div class="index__card-zakladka d-flex align-items-center justify-content-center">
                  <img src="/img/Suitcase.png" alt="">
                </div>
                <div class="index__card__header">
                  Мои счета
                  <hr>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="col-xl-2 col-12 d-flex flex-column">
          <div class="index__item rounded">
            <div class="index__item-header d-flex align-items-center justify-content-center">
              Курс обмена валют:
            </div>
          </div>
          <div class="index__item d-flex flex-column rounded">
            <div class="index__item-shadow" />
            <div class="index__item-img"><img class="rounded-top" src="/img/auto.png" alt=""></div>
            <button class="index__item-button rounded-bottom">Кредит Auto</button>
          </div>
          <div class="index__item d-flex flex-column rounded">
            <div class="index__item-shadow" />
            <div class="index__item-img"><img class="rounded-top" src="/img/deposit.png" alt=""></div>
            <button class="index__item-button rounded-bottom">Депозиты</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<style lang="scss">
.index{
  padding: 20px 0;
  &__card{
    min-height: 370px;
    background: #eaeaea;
    border: 1px solid white;
    position: relative;
    margin-bottom: 30px;
    &-zakladka{
      position: absolute;
      left: 10px;
      top: -3px;
      background: url(/img/zakladka.png) no-repeat;
      width: 28px;
      height: 60px;
    }
    &__header{
      font-size: 24px;
      color: $red;
      padding: 5px 10px 15px 50px;
      & hr {
        margin: 0;
        display: block;
        background: $red;
      }
    }
  }
  &__item{
    min-height: 170px;
    background: #eaeaea;
    border: 1px solid white;
    position: relative;
    margin-bottom: 15px;
    &-shadow{
      z-index: 100;
      display: block;
      position: absolute;
      top: 0;
      left: 0;
      border: 79px solid transparent;
      transition: .3s;
    }
    &:hover{
      cursor: pointer;
    }
    &:hover &-shadow{
      border-left: 79px solid rgba($color: #fff, $alpha: .15);
      border-top: 79px solid rgba($color: #fff, $alpha: .15);
    }
    &-header{
      padding: 10px;
      color: $color;
      font-size: 13px;
      font-weight: bold;
    }
    &-img{
      z-index: 2;
      height: 175px;
      & img{
        object-fit: cover;
        height: 100%;
        width: 100%;
      }
    }
    &-button{
      text-align: left;
      border: 0;
      background: $red;
      height: 100%;
      padding: 10px 15px;
      font-weight: bold;
      font-size: 12px;
      color: white;
    }
  }
}
</style>
