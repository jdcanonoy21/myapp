<script>
	export let value;
	export let disabled = false;
    export let color='';
    export let variant='';
    export let label;
	let clazz = '';
	export { clazz as class };
    

</script>


<option {value} class='{variant}-label input-text transition duration-200 text-2xl font-medium text-gray-700 text-opacity-80 absolute'>{label}</option>  
