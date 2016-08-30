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
  </div>
</template>

<script>
import WHeader from './components/w-header'
export default{
	components:{
		WHeader
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
