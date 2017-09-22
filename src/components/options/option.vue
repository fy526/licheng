<template>
	<div class="f_option">
		<ul class="myOptions">
			<li v-for="lis in list">
				<img :src="lis.URL">
				<p class="option_font"><a href="javascript:void(0)" class="myProfession">{{lis.name}}</a></p>
			</li>
			<!-- <li>		
				<img src="../../assets/myVideo.png">
				<p class="option_font"><a href="javascript:void(0)">我的视频</a></p>
			</li>
			<li>
				<img src="../../assets/wrong.png">
				<p class="option_font"><a href="javascript:void(0)">错题集</a></p>
			</li>
			<li>
				<img src="../../assets/msg.png">
				<p class="option_font"><a href="javascript:void(0)">消息</a></p>
			</li> -->
		</ul>
	</div>
</template>

<script>
import axios from 'axios'
	export default {
		name: 'f_option',
		data() {
			return {
				list: [],
			}
		},
		created() {
			const url = 'index.php?m=shop&c=index_interface&a=index';
			axios(url).then((res) => {
				console.log(res.data);
			})
		}

	}
</script>

<style>
	.myOptions{
		display: flex;
		flex-direction: row;
		justify-content: space-between;
    	padding: 0.2rem 0.3rem;
		border-bottom: 1px solid #e1e1e1;
		background-color: #fff;
	}
	.myOptions li>img{
		width:1rem;
		height:1rem;
	}
	.option_font{
		text-align: center;
		margin-top: 0.2rem;
	}
	.option_font>a{
		display: inline-block;
	}
</style>