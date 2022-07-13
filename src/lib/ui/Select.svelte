
<script>
	export let value;
	export let disabled = false;
    export let color='';
    export let variant='';
    export let label;
	let clazz = '';
	export { clazz as class };
    

</script>


<select {value} {label} class="{variant} m-4 h-[5rem] px-4 text-2xl border-gray-700 border-b-2 border-opacity-50 outline-none placeholder-gray-300 placeholder-opacity-0 ">
    <slot />
</select>
