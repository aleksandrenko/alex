<script>
	import Header from '../components/Header.svelte';
	import Toolbar from '../components/Toolbar.svelte';

	export let segment;
</script>

<style>
	app {
		position: fixed;
		top: 0;
		bottom: 0;
		left: 0;
		right: 0;
		display: flex;
		flex-direction: column;
	}

	main {
		flex: 1;
	}
</style>

<app>
	<Header {segment}/>

	<main>
		<slot></slot>
	</main>

	<Toolbar {segment} />
</app>