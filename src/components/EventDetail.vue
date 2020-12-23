<template>
<div>
	<label for="detail">イベントの内容</label>
	<pre>{{ value }}</pre>
	<textarea id="detail" cols="30" rows="10" @input="$emit('input', $event.target.value)"></textarea>
</div>
</template>

<script>
export default {
	props: ['value'],
}
</script>
