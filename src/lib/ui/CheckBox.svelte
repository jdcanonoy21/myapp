

<script>
	export let value;
	export let name = '';
	export let disabled = false;
    export let checked = false;
    export let color='';
    export let label='';
	let clazz = '';
	export { clazz as class };

    $: disabledClass = disabled ? 'text-gray-500' : '';
</script>


<label class='flex m-4'>
    <input 
    bind:value
    type="checkbox"
    {disabled}
    {name}
    {label}
    {checked}
    class="{color} w-8 h-8"
/>
    <span class="{disabledClass} text-2xl pl-2">{label}</span>
</label>

