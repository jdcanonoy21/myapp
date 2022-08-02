<script>
	
	let drawer;
	
	const openDrawer = ()=>{

		drawer.addEventListener('sl-hide', (event) => console.log('hide'));
		drawer.show();

	};
	
</script>

<button on:click={openDrawer}>Open</button>

<sl-drawer label="Drawer" class="drawer menu" bind:this={drawer}>

	<sl-select>
		<sl-menu-item value="option-1">Option 1</sl-menu-item>
		<sl-menu-item value="option-2">Option 2</sl-menu-item>
		<sl-menu-item value="option-3">Option 3</sl-menu-item>
	</sl-select>
	
</sl-drawer>

<svelte:head>


</svelte:head>