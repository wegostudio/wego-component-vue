<template>
	<button class="wego-button" :class="['wego-button-' + type, 'wego-button-' + size, {'disabled':disabled,'w-float-left':left, 'w-float-right':right}]" @touchstart="touchstart">
		<label class="wego-button-text">
			<slot></slot>
		</label>
	</button>
</template>
<script>
/**
 * w-border
 * @module components/button
 * @desc 按钮
 * @param {string} [type=default] - 按钮类型 有default, primary, plain, disable 可选
 * @param {boolean} [disabled=false] - 禁用
 * @param {boolean} [left=false] - 左浮动
 * @param {boolean} [right=false] - 右浮动
 * @param {string} [size = normal] - 尺寸 有 normal,small
 * @param {slot} - 按钮显示文字
 * 
 * @example
 * <w-button type="default" size="small" disabled>default</w-button>
 * <w-button type="primary" float>primary</w-button>
 * <w-button type="primary" floatright>primary</w-button>
 */
export  default {
	props: {
		disabled:Boolean,
		left:Boolean,
		right:Boolean,
		type:{
			type: String,
			default: 'default',
		},
		size: {
			size: String,
			default: 'normal',
		}
		
  },
  	methods: {
  		touchstart(self){
  			if (this.disabled){
	        		self.preventDefault();
	        		self.stopPropagation();
  			}
  		},
  	}
};
</script>

<style type="text/css">
	.w-float-left{
		float: left;
	}
	.w-float-right{
		float: right;
	}
	.wego-button-default{
		background-color: #FFFFFF;
		color: #428BCA;
		border: 0;
	}
	.wego-button-default:active{
		background-color: #428BCA;
		color: #FFFFFF;
	}
	.wego-button-primary{
		background-color: #428BCA;
		color: #FFFFFF;
		border: 0;
	}
	.wego-button-primary:active{
		background-color: #3B7DB6;
	}
	.wego-button-plain{
		border: 1px solid #428BCA;
		color: #428BCA;
		background: none;
	}
	.wego-button-plain:active{
		background-color: #e3eaf0;
	}
	.wego-button-disable{
		background-color: #FFFFFF;
		color: #767676;
		border: 0;
	}
	.wego-button-disable:active{
		background-color: #dcdcdc;
	}
	.wego-button{
		display: block;
		text-align: center;
		outline: 0;
		box-sizing: border-box;
	}
	.wego-button-normal{
		font-size: 16px;
		width: 100vw;
		height: 12.2vw;
		border-radius: 8px;
	}
	.wego-button-small{
		font-size: 14px;
		width: 30.5vw;
		height: 10.6vw;
		border-radius: 4px;
	}
</style>