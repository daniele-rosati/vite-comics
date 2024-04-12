<script>
  import AppHeader from "./components/AppHeader.vue"
	import AppCards from "./components/AppCards.vue"

	import AppContacts from "./components/AppContacts.vue"

	export default {
		components: {
			AppHeader,
			AppCards,
			AppContacts,
		},
	}
</script>

<template>
	<AppHeader></AppHeader>
	<main>
		<AppCards></AppCards>
		
	</main>
	<footer>
	
		<AppContacts></AppContacts>
	</footer>
</template>

<style lang="scss">
	@use "./style/generic";
</style>
