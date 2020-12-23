<template>
	<div>
		<pre>{{ value }}</pre>
		<label for="host">EventHost</label>
		<input type="text" id="host" @input="$emit('input', $event.target.value.trim())">
	</div>
</template>

<script>
export default {
	props: ['value']
}
</script>
