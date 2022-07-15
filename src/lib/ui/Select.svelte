
<script>
    export let placeholder = '';
	export let value;
    export let selected ='';
	export let disabled = false;
    export let color='';
    export let variant='';
    export let width='';
    export let label;
	let clazz = '';
	export { clazz as class };
    

</script>
<div class="m-4">
    <span class='ml-28 bg-white input-text left-0 transition duration-200 text-lg font-medium text-gray-700 text-opacity-80 absolute'>{placeholder}</span>
    <select bind:value={selected} {label} class="{variant} h-[5rem] w{width} px-4 text-2xl border-gray-700 border-b-2 border-opacity-50 outline-none placeholder-gray-300 placeholder-opacity-0" autofocus>
        {#if placeholder}
            <option value="" disabled selected>{placeholder}</option>
        {/if}
        <slot />
    </select>
</div>


<style>
    select:focus ~ .input-text{
      @apply text-blue-700 transform -translate-y-10 -translate-x-4 scale-75 visible;
    }
    select:not(:placeholder-shown) ~ .input-text{
      @apply transform  -translate-y-10 -translate-x-4 scale-75;
    }
  </style>