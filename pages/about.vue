<template>
  <div class="about">
    <div class="container">
      <h2 class="about-h2">10 юзеров из сервиса</h2>
      <div class="row">
        <div v-for="user in users" :key="`userId-${user.id}`" class="col-xl-4 col-12">
          <div class="user rounded">
            <div class="user-zakladka d-flex align-items-center justify-content-center">
              <img src="/img/Suitcase.png" alt="">
            </div>
            <div class="user__name">
              {{user.name}}
              <hr>
            </div>
            <div class="user__field d-flex flex-column">
              <span>Логин: {{user.username}}</span>
              <span>Email:{{user.email}}</span>
              <span>Адрес: {{user.address.city + ', ' + user.address.street}}</span>
              <span>Телефон: {{user.phone}}</span>
              <span>Сайт: {{user.website}}</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  async asyncData ({ $axios }) {
    const users = await $axios.$get('https://jsonplaceholder.typicode.com/users')
    return {
      users
    }
  },
  mounted () {
    console.log(this.users)
  }
}
</script>

<style lang="scss">
  .about{
    &-h2{
      color: $red;
      padding: 20px 0;
    }
  }
  .user{
    min-height: 250px;
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
    &__name{
      font-size: 24px;
      color: $red;
      padding: 5px 10px 15px 50px;
      & hr {
        margin: 0;
        display: block;
        background: $red;
      }
    }
    &__field{
      padding: 5px 20px;
      font-size: 16px;
      color: $color;
      & span{
        padding: 5px;
      }
    }
  }
</style>
