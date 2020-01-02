<template>
  <div class="footer">
    <router-link to="/home">消息</router-link>
    <router-link to="/mine">我的</router-link>
    <router-link to="/about">空间</router-link>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped lang="scss">
  .footer{
    width: 100%;
    height: 40px;
    display: flex;
    a{
      width: 33.3%;
      height: 40px;
      line-height: 40px;
      text-align: center;
      &.router-link-exact-active {
      color: #42b983;
      }
    }
  }
</style>