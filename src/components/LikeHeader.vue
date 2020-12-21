<template>
	<div>
		<h1>{{ headerText }}</h1>
		<slot name="test"></slot>
		<slot></slot>
	</div>
</template>

<script>
export default {
	props: ["headerText"]
}
</script>

<style scoped>

</style>
