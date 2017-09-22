<template>
	<div class="header_img">
		<swiper :options="swiperOption" :not-next-tick="notNextTick" ref="mySwiper">
		    <swiper-slide><img src="../../assets/banner.jpg" alt=""></swiper-slide>
		    <swiper-slide><img src="../../assets/banner.jpg" alt=""></swiper-slide>
		    <swiper-slide><img src="../../assets/banner.jpg" alt=""></swiper-slide>
		    <swiper-slide><img src="../../assets/banner.jpg" alt=""></swiper-slide>
	  	</swiper>
	</div>
</template>

<script>
import { swiper, swiperSlide } from 'vue-awesome-swiper'
import axios from 'axios'
export default{
	name:'header_img',
	data(){
		return{
		 	notNextTick: true,
        	swiperOption: {
		        autoplay: 3000,
        	}
		}
	},
	components: {
		swiper,
		swiperSlide
	},
		// created(){
		// 	new Promise((res,req)=>{
		// 		res()
		// 	}).then((res)=>{
		// 		alert(1)
		// 	}).then(()=>{
		// 		alert(2)
		// 	}).then(()=>{
		// 		alert(3)
		// 	})

		// this.$http({
		// 	method:"get",
		// 	data:{},//post的传参
		// 	params:{ },//get的传参
		// 	url:'index.php?m=shop&c=index_interface&a=index'
		// 	}).then((res)=>{
		// 	console.log(res)
		// 	})
		// }
}
</script>

<style lang="less">
	.header_img{
		img{
			width:100%
		}
	}
</style>