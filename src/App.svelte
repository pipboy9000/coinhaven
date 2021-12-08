<script>
	import SideMenu from "./SideMenu.svelte";
	import Nav from "./Nav.svelte";
	import Exchange from "./Exchhange.svelte";
</script>

<main>
	<SideMenu />
	<div class="mainPage">
		<Nav />
		<div class="content">
			<Exchange />
		</div>
	</div>
</main>

<style>
	:global(body) {
		padding: 0;
		margin: 0;
		background: #f7f7fb;
	}

	main {
		display: flex;
	}

	.mainPage {
		display: flex;
		flex-direction: column;
		width: 100%;
	}

	.content {
		padding: 24px;
		box-sizing: border-box;
		background: #f7f7fb;
	}
</style>
