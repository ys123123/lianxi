<template>
  <div class="home">
    <div class="top">
      消息
    </div>
    <input type="text" placeholder="搜索">
    <div class="lis" v-for="item in list" :key="item.index">
      <img :src="item.img" alt="" />
      <div class="name">{{item.name}}</div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      list: []
    }
  },
  created() {
    this.getList()
  },
  methods: {
    getList() {
      this.$http.get('/api/list').then(res=>{
        this.list = res.data.list
      })
    }
  },
}
</script>
<style lang="scss">
  .home{
    width: 100%;
    height: 100%;
    .top{
      width: 100%;
      height: 60px;
      background: skyblue;
      line-height: 60px;
      text-align: center;
      font-size: 16px;
      color: #fff;
    }
    .lis{
      width: 100%;
      height: 100px;
      display: flex;
      margin-top: 10px;
      border-bottom: 1px solid #eee;
      img{
        width: 100px;
        height: 100px;
        border-radius: 50%;
      }
      .name{
        width: 300px;
        padding-left: 30px;
        line-height: 100px;
      }
    }
  }
</style>
