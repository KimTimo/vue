<template>
	<div>
<<<<<<< HEAD
		<h2>보간법</h2>
		<p>{{ message }}</p>
		<p v-once>{{ message }}</p>
		<button v-on:click="message = message + `!`">click</button>
		<hr />
		<h2>v-html</h2>
		<p>{{ rawHtml }}</p>
		<p v-html="rawHtml"></p>
=======
		<p>
			{{ counter }}
		</p>
		<p>
			{{ message }}
		</p>
		<button @click="increment">click</button>

		<div v-bind:title="dynamicTitle">마우스를 올려보세요!!!</div>
		<div>
			<input type="text" v-bind:disabled="isInputDisabled" />
		</div>
>>>>>>> refs/remotes/origin/main
	</div>
</template>

<script>
import { ref } from 'vue';

export default {
	setup() {
<<<<<<< HEAD
=======
		const isInputDisabled = true;
		const counter = ref(0);
>>>>>>> refs/remotes/origin/main
		const message = ref('Hello Vue3');
		const rawHtml = ref('<strong>안녕하세요</strong>');
		return {
<<<<<<< HEAD
=======
			isInputDisabled,
			counter,
>>>>>>> refs/remotes/origin/main
			message,
			rawHtml,
		};
	},
};
</script>

<style lang="scss" scoped></style>
