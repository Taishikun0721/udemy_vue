<template>
	<div>
		<slot name="condition"></slot>
		<input type="checkbox" id="10" value="10代" @input="$emit('input', $event.target.value)">
		<label for="10">10代</label>
		<input type="checkbox" id="20" value="20代" @input="$emit('input', $event.target.value)">
		<label for="20">20代</label>
		<input type="checkbox" id="30" value="30代" @input="$emit('input', $event.target.value)">
		<label for="30">30代</label>
		<h1>{{ eventData.target }}</h1>
	</div>
</template>

<script>
export default {
	props: ['value']
}
</script>
