<template>
 <div class="banner">
    <ul class="clearfix">
	<router-link
	v-for="item of data"
	:key="item._id"
	:to="{name:'detail',params:{_id:item._id},query:{apiName:apiName}}"
		
	tag="li"
	>
		<img :src="item.banner" alt=""/>
		<div class="text-box">
					  <h2>{{item.title}}</h2>
					  <p>{{item.sub_title}}</p>
		</div>
	</router-link>
     
      <!-- <li><img src="/images/img_2.jpg" alt=""/>
        <div class="text-box">
          <h2>还可以降低首付款健身房2222</h2>
          <p>刘德华22 / 文</p>
        </div>
      </li>
      <li><img src="/images/img_3.jpg" alt=""/>
        <div class="text-box">
          <h2>还可以降低首付款健身房333</h2>
          <p>刘德华33 / 文</p>
        </div>
      </li>
      <li><img src="/images/img_1.jpg" alt=""/>
        <div class="text-box">
          <h2>还可以降低首付款健身房11111</h2>
          <p>刘德华11 / 文</p>
        </div>
      </li> -->
    </ul>
  </div>
</template>

<script>
	import Swipe from '../assets/js/swipe.js'
	import $ from 'jquery';
	
  export default {
    name:'swiper',
    props:[
		'data','apiName'
	],
    data(){
      return {
        
      }
    },
    components:{},
    mounted(){
		console.log("mounted");
		var mySwipe=new Swipe($('.banner')[0],{
		  auto:2000,
		  continuous:true,
		  stopPropation:true,
		  callback:function (index,element){
		    $('.banner ol li').removeClass('active');
		    $('.banner ol li').eq(index).addClass('active');
		  }
		})
	},
    updated(){
		console.log("updated");
	},
    methods:{}
  }
</script>

<style>
  .banner{margin-top:0.6rem;position: relative;overflow: hidden; z-index: 1}
  .banner ul li{width:6.4rem;float:left;position: relative;}
  .banner ul li img{width:100%; display:block;}
  .banner ul li .text-box{width:5.8rem; padding:0 0.3rem;height:1.24rem; position:absolute; left:0; bottom:0; color:#fff; background:rgba(0,0,0,0.5);}
  .text-box h2{ font-size:0.3rem; font-weight:normal; margin-top:0.22rem; line-height:100%; margin-bottom:0.22rem; overflow:hidden;white-space:nowrap;text-overflow:ellipsis;}
  .text-box p{ line-height:100%;}
  
  .banner ol{position:absolute; right:0.2rem;bottom:0.2rem;}
  .banner ol li{width:0.15rem;height:0.15rem; background:#5477b2; float:left; border-radius:50%; margin-right:0.08rem;}
  .banner ol li.active{ background:#fff;}
</style>
