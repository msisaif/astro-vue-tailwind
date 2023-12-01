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
			class="flex items-center justify-between rounded-md border border-[#42b883] px-3 py-2 text-[#42b883] transition-all hover:scale-105"
		>
			<div>Counter</div>
			<div class="flex items-center justify-center gap-1">
				<svg class="h-6 w-auto shrink-0 grow-0" viewBox="0 0 128 128">
					<path
						fill="#42b883"
						d="M78.8,10L64,35.4L49.2,10H0l64,110l64-110C128,10,78.8,10,78.8,10z"
					></path>
					<path fill="#35495e" d="M78.8,10L64,35.4L49.2,10H25.6L64,76l38.4-66H78.8z"></path>
				</svg>
				<b>Vue.js</b>
			</div>
			<span class="select-none">&rarr;</span>
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
			<div class="select-none text-4xl font-bold">
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
