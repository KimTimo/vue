<template>
	<div>
		<h2>보간법</h2>
		<p>{{ message }}</p>
		<p v-once>{{ message }}</p>
		<button v-on:click="message = message + `!`">click</button>
		<hr />
		<h2>v-html</h2>
		<p>{{ rawHtml }}</p>
		<p v-html="rawHtml"></p>
		<hr />
		<h2>속성 바인딩</h2>
		<div title="안녕하세요.">마우스를 올려보세요</div>
		<div :title="dynamicTitle">마우스를 올려보세요</div>
		<input type="text" value="안꼬몽" v-bind:disabled="isInputDisabled" />
		<input v-bind="attrs" />
		<h2>JavaScript</h2>
		{{ message.split('').reverse().join('') }}<br />
		{{ isInputDisabled ? `예` : `아니오` }}
	</div>
</template>

<script setup>
import { ref } from 'vue';

const message = ref('Hello Vue3');
const rawHtml = ref('<strong>안녕하세요</strong>');

const dynamicTitle = ref(`안녕하세요`);
const isInputDisabled = ref(true);
const attrs = ref({
	type: `text`,
	value: `1231231`,
	disabled: false,
});
</script>

<style lang="scss" scoped></style>
