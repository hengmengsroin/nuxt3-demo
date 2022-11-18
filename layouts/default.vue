<script setup>
const menuItems = [{
	name: "Dashboard",
	path: "/dashboard",
	icon: "mdi:view-dashboard",
	active: true,
},
{
	name: "About",
	path: "/about",
	icon: "mdi:alert-box-outline"
},
{
	name: "Users",
	path: "/user",
	icon: "mdi:account-supervisor"
}]
</script>

<template>
	<div class="box">
		<!-- <div class="nav">
			<div class="logo">
				<div class="title">NATIONAL SOCIAL</div>
				<div class="title">PROTECTION</div>
				<div class="title green">REGISTRY</div>
			</div>
			<NuxtLink :to="item.path" class="menu-item" v-for="item of menuItems"
				:class="{ active: $route.path == item.path }" :key="item.name">
				<Icon :name="item.icon" size="24" />
				<div class="name">
					{{ item.name }}
				</div>
			</NuxtLink>
		</div>
		<div class="main">

			<div class="title">{{ menuItems.find(item => item.path == $route.path).name }}</div>
			<slot />
		</div> -->
		<slot />
	</div>
</template>
<style scoped lang="scss">
.box {
	display: flex;
	width: 100%;
	height: 100%;
	background-color: #EEF7F0;
	padding: 20px;

	.nav {
		width: 300px;
		padding: 20px;
		background-color: linear-gradient(121.56deg, #FFFFFF 8.05%, #F1F9F3 82.51%);
		border: 1px solid #FFFFFF;
		border-radius: 30px;
		display: flex;
		flex-direction: column;

		.logo {
			display: flex;
			flex-direction: column;
			justify-items: center;
			align-items: center;
			margin: 10px 0 30px 0;

			.title {
				font-size: 20px;
				color: black;
				font-weight: 700;

			}

			.green {
				color: green
			}
		}

		.menu-item {
			width: 100%;
			padding: 16px 20px;
			cursor: pointer;
			margin-top: 4px;
			margin-bottom: 4px;
			border-radius: 18px;
			display: flex;
			flex-direction: row;

			&:hover {
				border-radius: 18px;
				background: rgba(40, 199, 148, 0.15);

			}

			.name {
				margin-left: 10px;
			}
		}

		.active {
			border-radius: 18px;
			background: rgba(40, 199, 148, 0.15);
			color: rgb(0, 170, 43);
			font-weight: bold;
			border: 0.5px solid rgb(0, 170, 43, 0.2);
		}
	}

	.main {
		width: 100%;
		height: 100%;
		padding-left: 20px;

		.title {
			font-size: 30px;
			font-weight: bold;
			color: green;
			padding-bottom: 10px;
		}
	}


}
</style>