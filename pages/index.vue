<script setup>

let myObject = {
	firstName: "hello",
	lastName: "mengsroin",
	gender: "M"
}
let message = useState('message', () => "gekki");

const onClick = () => [
	message = "hi"
]
</script>
<template>
	<div>
		<h1>Welcome to the homepage</h1>
		<AppAlert title="This is title from index js" :likes="12">
			This is an auto-imported component
		</AppAlert>
		<NuxtLink to="/about">About</NuxtLink>
	</div>
	<div>
		<li v-for="(value, key, index) in myObject">
			{{ index }}. {{ key }}: {{ value }}
		</li>
	</div>
	<div>
		<p>Message is: {{ message }}</p>
		<input v-model="message" placeholder="edit me" />
	</div>
	<NButton @click="onClick">Hi</NButton>
	<NCard n="green-500">
		<!-- both of them are themed green -->
		<NCheckbox>i accept the terms & conditions</NCheckbox>
		<NButton>Submit</NButton>
	</NCard>
</template>
