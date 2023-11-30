<script setup>
import { ref } from 'vue'

const props = defineProps({
	initialValue: {
		type: Number,
		default: 0
	}
})

const counter = ref(props.initialValue)

function increment() {
	counter.value++
}

function decrement() {
	counter.value--
}
</script>

<template>
	<div class="rounded-lg bg-gray-600 p-4 text-white">
		<a
			href="https://vuejs.org/"
			target="_blank"
			class="flex items-center justify-between rounded-md bg-green-600 px-3 py-2"
		>
			<div>This component by <b>Vue.js</b></div>
			<span>&rarr;</span>
		</a>
		<div class="mt-3 flex items-center justify-center gap-4">
			<svg
				xmlns="http://www.w3.org/2000/svg"
				fill="none"
				viewBox="0 0 24 24"
				stroke-width="1.5"
				stroke="currentColor"
				class="h-10 w-10 cursor-pointer"
				@click="decrement"
			>
				<path
					stroke-linecap="round"
					stroke-linejoin="round"
					d="M15 12H9m12 0a9 9 0 11-18 0 9 9 0 0118 0z"
				/>
			</svg>
			<div class="text-4xl font-bold">
				{{ counter }}
			</div>
			<svg
				xmlns="http://www.w3.org/2000/svg"
				fill="none"
				viewBox="0 0 24 24"
				stroke-width="1.5"
				stroke="currentColor"
				class="h-10 w-10 cursor-pointer"
				@click="increment"
			>
				<path
					stroke-linecap="round"
					stroke-linejoin="round"
					d="M12 9v6m3-3H9m12 0a9 9 0 11-18 0 9 9 0 0118 0z"
				/>
			</svg>
		</div>
	</div>
</template>
