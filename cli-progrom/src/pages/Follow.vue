<template>
  <div class="Follow">
    <Cell :data="{id:0,title:'alerc',des:'001'}" apiName="follow"/>
	<Cell :data="{id:0,title:'alerc',des:'001'}" apiName="follow"/>
	<Cell :data="{id:0,title:'alerc',des:'001'}" apiName="follow"/>
	<Cell :data="{id:0,title:'alerc',des:'001'}" apiName="follow"/>
    
  </div>
</template>

<script>
	import Cell from '../components/Cell.vue'
  export default {
    name:'Follow',
    props:{},
    data(){
      return {
        
      }
    },
    components:{
		Cell
	},
    mounted(){},
    updated(){},
    methods:{}
  }
</script>

<style scoped>
  .Follow{
	  margin-top:0.5rem;
	  margin-left: 0.4rem;
	  margin-right: 0.4rem;
  }
</style>
