<template>
	<a class="wego-tab-item"
		@click="$parent.selected = id"
		:class="{'isselected':$parent.selected === id}">
		<div class="wego-tab-item-title">
			<slot></slot>
		</div>
	</a>
</template>

<script>
export  default {
	props: {
		id: ''
	}
};
</script>

<style type="text/css">
	
</style>