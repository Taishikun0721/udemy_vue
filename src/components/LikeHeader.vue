<template>
	<div>
		<h1>{{ headerText }}</h1>
		<slot name="test">aaaa</slot>
		<slot name="taishiro"></slot>
	</div>
</template>

<script>
export default {
	props: {
		headerText: {
			type: String
		}
	}
}
</script>

<style scoped>

</style>
