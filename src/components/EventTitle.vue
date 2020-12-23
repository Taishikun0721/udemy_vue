<template>
	<div>
		<h2>{{ value }}</h2>
		<label for="title">EventTitle</label>
		<input type="text" id="title" @input="$emit('input', $event.target.value)">
	</div>
</template>

<script>
export default {
	props: ['value']
}
</script>
