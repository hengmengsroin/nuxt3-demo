<script>
export default {
	props: {
		title: String,
		likes: Number
	}
}

</script>
<template>
	<div class="title">{{ title }}</div>
	<div>{{ likes }}</div>
	<div>
		<slot />
	</div>
</template>

<style scoped >
.title {
	border: 1px solid blue;
	color: orange;
}
</style>