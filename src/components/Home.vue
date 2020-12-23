<template>
	<div>
		<h2 v-border:solid.round="{ width: '5px', color: 'brown'}">Home</h2>
		<h2>{{ title | lowerCase }}</h2>
		<h2>{{ subTitle | lowerCase }}</h2>
	</div>
</template>

<script>
export default {
	data() {
		return {
			tmpData: "hello",
			title: "welcome to Tokyo",
			subTitle: "Tokyo is a great city"
		}
	},
	filters: {
		lowerCase(value) {
			return value.toLowerCase();
		}
	}
}
</script>
