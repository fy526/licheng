<template>
	<div class="f_content" >
		<div v-for="box in 4" class="content_module"> 
			<div class="content_title">
				<div></div>
				<a href="javascript:void(0)">推荐视频</a>
			</div>
			<ul>
				<li v-for="item in 4">
					<div class="content_video">
						<a href="javascript:void(0)"><img src="../../assets/4.jpg" alt=""></a>
						<h3>专业指导</h3>
						<div class="video_intro">
							<span>￥139.00</span>
							<div>
								<img src="../../assets/love.png" alt=""><span>1.3万</span>
								<img src="../../assets/comment.png" alt=""><span>596</span>
							</div>
						</div>
					</div>
				</li>
				 
			</ul>
		</div>
	</div>
</template>
<script>
	import axios from 'axios'
	export default{
		name:'f_content',
		data(){
			return{

			}
		},
		created(){
			const url='index.php?m=shop&c=index_interface&a=index';
			axios(url).then((res)=>{
				console.log(res);
			})

		}
	}
</script>

<style>
	.f_content{
		margin-top: 0.2rem;
		padding-bottom: 0.23rem;
	}
	.f_content>div{
		padding-top: 0.23rem;
	}
	.content_module{
		margin-top: 0.23rem;
		background-color: #fff;
		padding-bottom: 0.23rem;
	}
	.content_title{
		margin-left: 0.23rem;
	}
	.content_title>div{
		display: inline-block;
		height:0.26rem;
		border-left:5px solid #2d50b6;
	}
	.f_content ul{
		display: flex;
		flex-direction: row;
		flex-wrap: wrap;
	}
	.f_content ul li{
		margin-left: 0.23rem;
	}
	.content_video{
		width:3.4rem;
		text-align: justify;
		margin-top: 0.2rem;
	}
	.content_video>h3{
		padding:0.1rem 0;
	}
	.content_video a img{
		width:3.4rem;
	}
	.video_intro{
		display: flex;
		justify-content: space-between;
	}
	.video_intro div>img{
		width:0.2rem;
	}
	.video_intro>span{
		color:#c62b30;
	}
</style>