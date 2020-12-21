<template>
<div>
  <p>いいね({{ halfNumber }})</p>
  <p>{{ testProps }}</p>
  <button @click="increment">button1</button>
</div>
</template>

<script>
export default {
  props: ["totalNumber"],
  computed: {
    halfNumber() {
      return this.totalNumber / 2
    }
  },
  methods: {
		increment() {
      this.$emit("increment-click", this.totalNumber + 1);
		}
	}
};
</script>


<style scoped>
 </style>
