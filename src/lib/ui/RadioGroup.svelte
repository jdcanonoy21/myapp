<script>
	export let name = '';
    export let defaultValue='';
	let clazz = '';
	export { clazz as class };


</script>


<div {name} {defaultValue}>
    <slot />
</div>