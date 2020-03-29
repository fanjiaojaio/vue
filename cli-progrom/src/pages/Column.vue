<template>
  <div class="Column">
    <Cell :data="{id:0,title:'alerc',des:'001'}"  apiName="column"/>
	<Cell :data="{id:0,title:'alerc',des:'001'}"  apiName="column"/>
	<Cell :data="{id:0,title:'alerc',des:'001'}"  apiName="column"/>
	<Cell :data="{id:0,title:'alerc',des:'001'}"  apiName="column"/>
  </div>
</template>

<script>
	import Cell from '../components/Cell.vue'
  export default {
    name:'Column',
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
  .Column{
	  margin-top:0.5rem;
	  margin-left: 0.4rem;
	  margin-right: 0.4rem;
  }
</style>
