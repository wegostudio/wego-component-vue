<template>
  <div id="app">
  	<w-header title = "头部标题">
  		<div slot="right">返回</div>
  	</w-header>
  	<w-header title = "头部标题">
  		<div slot="right">
  			<img src="logo.png"/>
  		</div>
  	</w-header>
  	<br />
  	<w-button type="default" disabled>default</w-button>
  	<br />
  	<w-button type="primary" float>primary</w-button>
  	<br />
  	<w-button type="plain">plain</w-button>
  	<br />
  	<w-button type="disable">disabel</w-button>
  	<br />
  	<w-button type="default" size="small">default</w-button>
  	<w-button type="primary" size="small">primary</w-button>
  	<div>
  	<w-button type="plain" size="small" left>plain</w-button>
  	<w-button type="disable" size="small" right>disabel</w-button>
  	</div>
  	<br />
  	<br />
  	<br />
  	<w-input title="日期" type="date"></w-input>
  	<br />
  	<w-input title="输入数字" placeholder="请填写数字" type="number"></w-input>
  	<br />
  	<w-input title="输入密码" placeholder="请输入密码" type="password"></w-input>
  	<br />
  	<w-input title="输入框" placeholder="请填写你的内容" type="text"></w-input>
  </div>
</template>

<script>
import WHeader from './components/w-header'
import WButton from './components/w-button'
import WInput from './components/w-input'
export default{
	components:{
		WHeader,
		WButton,
		WInput,
	}
}
</script>


<style>
/*@import url("http://yui.yahooapis.com/pure/0.6.0/base-min.css");*/
@import url("styles/grids.css");
/*@import url("http://yui.yahooapis.com/pure/0.6.0/pure-min.css");*/
/*body {
  font-family: Helvetica, sans-serif;
}*/
</style>
