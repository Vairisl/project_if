<template>
	<ul>
		<li v-for="item in menu"
			v-bind:class="{ active: item.active}"
			@click="goToPage(item)">
			{{item.title}}
		</li>
	</ul>
</template>

<script>
export default {
	data () {
		return {
			menu: [
				{
					title: "Home",
					active: true,
				},
				{
					title: "Contacts",
					active: false,
				},
			]
		}
	},
	methods: {
		goToPage(menuItem) {
			for (let i in this.menu) {
				this.menu[i].active = false
			}
			
			menuItem.active = true
		}
	}
}
</script>

<style>
.active {
	color: red;
}

li:hover {
	color: blue;
}
</style>

