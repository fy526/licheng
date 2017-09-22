<template>
	<div class="f_notice">
		<span>公告:</span>
		<swiper :options="swiperOption" :not-next-tick="notNextTick" ref="mySwiper">
		    <swiper-slide><a href="javascript:void(0)">{{msg}}</a></swiper-slide>
		    <swiper-slide><a href="javascript:void(0)"></a></swiper-slide>
	  	</swiper>
	</div>
</template>

<script>
import axios from 'axios'
	import { swiper, swiperSlide } from 'vue-awesome-swiper'
	export default{
		name:'f_notice',
		data(){
			return{
			 	notNextTick: true,
        		swiperOption: {
		          	autoplay: 2000,
		          	direction : 'vertical',
        		},
        		msg:''
			}
		},
		components: {
			swiper,
			swiperSlide
		},
		created(){
			const url='index.php?m=shop&c=index_interface&a=index';
			axios(url).then((res)=>{
				console.log(res);
				console.log(res.data.datas.article_list[1].article_title)
				this.msg=res.data.datas.article_list[1].article_title
			})
		}
	}
</script>
<style>
	.f_notice{
		background-color: #fff;
		height:0.72rem;
		display:flex;
		/*justify-content: space-between;*/
		align-items: center;
		background-image:url('../../assets/affiche.png');
		background-repeat: no-repeat;
		background-position: 0.3rem 0rem;
	}
	.f_notice>span{
		padding-left:1.2rem;
		font-size: 0.3rem;
	}
	.f_notice .swiper-container{
		height:0.72rem;
		margin-top: ;
		flex-basis: auto;
		margin: 0.4rem 0.2rem 0 0.2rem;
	}
</style>