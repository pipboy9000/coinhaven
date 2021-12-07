<script>
	import SideMenu from "./SideMenu.svelte";
	import Nav from "./Nav.svelte";
</script>

<main>
	<SideMenu />
	<Nav />
	<div class="content" />
</main>

<style>
	:global(body) {
		padding: 0;
		margin: 0;
	}

	main {
		display: flex;
	}
</style>
