<template>
	<div>
		<h2>{{ value }}</h2>
		<input type="checkbox" @input="$emit('input', !value)">
	</div>
</template>

<script>
export default {
	props: ['value']
}
</script>
