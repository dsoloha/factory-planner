<script>
	import Draggable from '../components/draggable.svelte';
</script>

<main>
	<h1>Factory Planner</h1>

	<Draggable>Drag Me</Draggable>
</main>

<style>
	@media (prefers-color-scheme: dark) {
		:root {
			background-color: black;
			color: white;
		}
	}
</style>
