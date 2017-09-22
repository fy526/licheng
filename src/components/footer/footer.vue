<template>
	<div class="f_footer">
		<ul class="footer_item">
			<li class="active">
				<a href="javascript:void(0)">
					<img src="../../assets/index_logo.png" alt="">
					<h5>首页</h5>
				</a>
			</li>
			<li>				
				<a href="javascript:void(0)">
					<img src="../../assets/video_logo.png" alt="">
					<h5>视频中心</h5>
				</a>
			</li>
			<li>
				<a href="javascript:void(0)">
					<img src="../../assets/test_logo.png" alt="">
					<h5>考试中心</h5>
				</a>
			</li>
			<li>
				<a href="javascript:void(0)">
					<img src="../../assets/man_logo.png" alt="">
					<h5>我的</h5>
				</a>
			</li>
		</ul>
	</div>
</template>
<script>
	export default{
		name:'f_footer'
	}
</script>
<style>
	.footer_item{
		display: flex;
		justify-content: space-between;
	}
	.footer_item img{
		width:0.48rem;
		height:0.42rem;
	}
	.footer_item h5{
		color:#555;
		font-weight: normal;

	}
	.footer_item li{
		width:25%;
	}
	.footer_item li:active a{
		color:#2d50b6;
	}
	.footer_item a{
		display: inline-block;
		width:100%;
		text-align: center;
	}
	.footer_item li.active a{
		color:#2d50b6;;
	}
</style>