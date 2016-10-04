<template>
	<ul>
		<li v-for="item in menu"
			v-bind:class="{ active: item.active}">
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
	}
}
</script>

<style>
.active {
	color: red;
}
</style>

