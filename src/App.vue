<script>
	import AppHeader from "./components/AppHeader.vue"
	import AppCards from "./components/AppCards.vue"
	import AppIcons from "./components/AppIcon.vue"
	import AppNav from "./components/AppNav.vue"
	import AppContacts from "./components/AppContacts.vue"

	export default {
		components: {
			AppHeader,
			AppCards,
			AppIcons,
			AppNav,
			AppContacts,
		},
	}
</script>

<template>
	<AppHeader></AppHeader>
	<main>
		<AppCards></AppCards>
		<AppIcons></AppIcons>
	</main>
	<footer>
		<AppNav></AppNav>
		<AppContacts></AppContacts>
	</footer>
</template>

<style lang="scss">
	@use "./style/generic";
</style>