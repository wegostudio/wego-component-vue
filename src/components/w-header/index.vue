<template>
	<header class="wego-header pure-g">
		<div class="pure-u-1-2">
			<div class="wego-header-title" v-text = "title"></div>
			<slot name = "left"></slot>
		</div>
		<div class="pure-u-1-2">
			<div class="wego-header-right w-right">
				<slot name="right"></slot>
			</div>
		</div>
	</header>
</template>


<script>
/**
 * w-header
 * @module components/header
 * @desc 顶部导航
 * @param {string} [title] - 标题
 * @param {slot} [left] - 定制左侧区域内容（此时不设置title属性）
 * @param {slot} [right] - 定制右侧区域内容
 * 
 * @example
 * <w-header title = "文字标题">
 *   <div slot="right">返回</div>
 * </w-header>
 * 
 * <w-header title = "首页">
 *   <div slot="right">
 * 	   <img src="logo.png" />
 *   </div>
 * </w-header>
 * 
 * <w-header>
 *		<div slot="left">
 * 			<img src="logo.png"/>
 * 		</div>
 * 		<div slot="right">
 * 			头部标题
 * 		</div>
 * 	</w-header>
 */

export default {
	props: {
		title: String
	},
};
</script>
<style type="text/css">
	@import url("../../styles/grids.css");
	.w-right{
		text-align: right;
	}
	.wego-header{
		background-color: #FFFFFF;
		width:100vw;
		height: 12.5vw;
	}
	.wego-header-title{
		font-family: SourceHanSansSC-Normal;
		padding-left: 4vw;
		line-height: 12.5vw;
		font-size: 18px;
		color: #428BCA;
	}
	.wego-header-right{
		opacity: 0.53;
		font-family: SourceHanSansSC-Normal;
		padding-right: 4vw;
		line-height: 12.5vw;
		font-size: 14px;
		color: #000000;
	}
	.wego-header-right img{
		width: 20vw;
		height: 12.5vw;
	}
	
</style>