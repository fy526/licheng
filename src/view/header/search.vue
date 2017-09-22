<template>
	<div class="search">
		<img src="../../assets/logo.png" alt="" class="f_logo">
		<input type="text" placeholder="搜索专业/视频">
	</div>
</template>

<script>
	export default{
		name:'search'
	}
</script>

<style>
	.search{
		width:100%;
		height:1.22rem;
		display: flex;
		background-color: #fff;
		align-items: center;justify-content: center;
	}
	.f_logo{
		height: 0.7rem;
		width:0.98rem;
	}
	.search>input{
		display: inline-block;
		margin-left: 0.2rem;
	    background-color: #eeeff3;
	    height: 0.8rem;
	    width:55%;
	    border-color: #eeeff3;
	    border-radius: 5px;
	    border:1px solid #eeeff3;
	    background-image: url('../../assets/search.png');
	    background-repeat: no-repeat;
	    background-position:0.3rem 0rem;
	    padding-left: 1.3rem;
	    outline: none;
	}
</style>