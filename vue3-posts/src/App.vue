<template>
	<div>
		<p>
			{{ counter }}
		</p>
		<p>
			{{ message }}
		</p>
		<button @click="increment">click</button>

		<div v-bind:title="dynamicTitle">마우스를 올려보세요.</div>
		<div>
			<input type="text" v-bind:disabled="isInputDisabled" />
		</div>
	</div>
</template>

<script>
import { ref } from 'vue';

export default {
	setup() {
		const isInputDisabled = true;
		const counter = ref(0);
		const message = ref('Hello Vue3');
		const increment = () => {
			counter.value++;
		};
		return {
			isInputDisabled,
			counter,
			message,
			increment,
		};
	},
};
</script>

<style lang="scss" scoped></style>
