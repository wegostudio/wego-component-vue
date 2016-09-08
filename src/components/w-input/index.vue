<template>
	<div class="wego-input">
		<div class="wego-input-title pure-u-3-12" v-text="title"></div>
		<div class="wego-input-value pure-u-8-12">
			<input class="wego-input-core" :placeholder="placeholder" :type="type"/>
		</div>
	</div>
</template>

<script>
/**
 * w-input
 * @desc 输入框
 * @param {string} [title] - 标题
 * @param {string} [placeholder] - 输入提示
 * @param {string} [type=text] - 内容类型 有data, number, password, text 等
 */
export default {
	props: {
		title: String,
		placeholder: String,
		type: {
			type: String,
			default: 'text'
		},
	}
}
</script>
<style type="text/css">
	.wego-input{
		width: 100vw;
		height: 12.5vw;
		clear: both;
		background: #FFFFFF;
		padding: 5px;
		line-height: 12.5vw;
	}
	.wego-input-title{
		font-size: 14px;
		color: #383838;
	}
	.wego-input-value{
		font-size: 14px;
		color: #bdbdbd;
	}
	.wego-input-core{
		outline: 0;
		width: 100%;
	}
</style>