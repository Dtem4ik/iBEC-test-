<template>
  <nav class="nav">
    <div class="container">
      <div class="row">
        <div class="col-xl-1 col-2">
          <img class="avatar" src="/img/red.png" alt="">
        </div>
        <div style="padding-left: 30px;" class="col-xl-11 col-10 d-flex flex-column align-items-start justify-content-around">
          <h3 class="nav-h3">My Account</h3>
          <ul class="nav__menu rounded">
            <li>
              <nuxt-link to="/">Главная</nuxt-link>
              <span />
            </li>
            <li>
              <nuxt-link to="/about">О нас</nuxt-link>
              <span />
            </li>
            <li>
              <nuxt-link to="/contact">Контакты</nuxt-link>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </nav>
</template>

<script>
export default {

}
</script>
<style lang="scss">
.nav{
  padding: 20px 0;
  .avatar{
    width: 97px;
    height: 97px;
  }
  &-h3{
    padding-left: 5px;
    color: $red;
    font-size: 24px;
  }
  &__menu{
    width: 100%;
    background: url(/img/RoundedMenu.png) no-repeat;
    background-size: 100%;
    & li{
      height: 48px;
      transition: .1s;
      display: flex;
      position: relative;
      // border-right: 1px solid #a7a7a7;
      & span{
        align-self: center;
        position: absolute;
        right: 0;
        display: flex;
        height: 60%;
        width: 2px;
        background: #a7a7a7;
        border-radius: 80%;
      }
      &:last-child{
        border: 0;
      }
      & a{
        padding: 0 37px;
        display: flex;
        align-items: center;
        justify-content: center;
        width: 100%;
        height: 100%;
        position: relative;
        text-decoration: none;
        color: $color;
        &:hover, &.nuxt-link-exact-active{
          background: url('/img/Layer2copy.png') no-repeat;
          background-position: 0px 100%;
          background-size: 100%;
          cursor: pointer;
        }
      }
    }
  }
}
@media (max-width: 1024px){
  .nav{
    .avatar{
      width: 67px;
      height: 67px;
    }
    &__menu{
      width: 100%;
      background: url(/img/RoundedMenu.png) no-repeat;
      background-size: auto;
      // flex-direction: column;
      & li{
        height: 48px;
        // border: 0;
        & a{
          font-size: 14px;
          padding: 0 15px;
        }
      }
    }
  }
}
</style>
