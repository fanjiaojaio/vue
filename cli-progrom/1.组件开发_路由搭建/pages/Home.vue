<template>
  <div class="Home">
    
    <swiper
      :data="[
        {_id:'5da99aed6947891e780cea7a',title:'xxx',sub_title:'xxx123',banner:'/images/img_1.jpg'},
        {_id:'5da99aed6947891e780cea7b',title:'xxx2',sub_title:'xxx1234',banner:'/images/img_1.jpg'},
      ]"
      apiName="banner"
    />
    
    <div class="home-m-l-r">
      <!-- <Cell :data="{_id:2342343,title:'啥地方',des:'撒打发斯蒂芬'}"/> -->
      <!-- <Cell :index="0" :data="{_id:2342343,title:'啥地方',des:'撒打发斯蒂芬'}"/> -->
      <Cell
        v-for="(item,index) of list"
        :key="item._id"
        :data="item"
        :index="index"
        api-name="home"
      />
    </div>
    
    
  </div>
</template>

<script>
  import swiper from '../components/swiper.vue'
  import Cell from '../components/Cell.vue'
  export default {
    name:'Home',
    props:{},
    data(){
      return {
        list:[
          {_id:1,title:'alex1',des:'ooo1'},
          {_id:2,title:'alex2',des:'ooo2'},
          {_id:3,title:'alex3',des:'ooo3'},
        ]
      }
    },
    components:{
      swiper,Cell
    },
    mounted(){},
    updated(){},
    methods:{}
  }
</script>

<style scoped>
  .Home{
    /* background: #999999; */
  }
  .home-m-l-r{
    margin: 0 0.4rem;
  }
</style>
