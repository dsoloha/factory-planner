<script lang="ts">
	export let left = 100;
	export let top = 100;

	let moving = false;

	function onMouseDown(): void {
		moving = true;
	}

	function onMouseMove(e: MouseEvent): void {
		if (moving) {
			left += e.movementX;
			top += e.movementY;
		}
	}

	function onMouseUp(): void {
		moving = false;
	}
</script>

<section on:mousedown={onMouseDown} style="left: {left}px; top: {top}px;" class="draggable">
	<slot />
</section>

<svelte:window on:mouseup={onMouseUp} on:mousemove={onMouseMove} />

<style>
	.draggable {
		user-select: none;
		cursor: move;
		border: solid 1px gray;
		position: absolute;
	}
</style>
