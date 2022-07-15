<script>
    import { onMount } from 'svelte';
	export let value;
	export let placeholder = '';
	export let disabled = false;
    export let color='';
    export let width='';
    export let helperText='';
    export let variant='';
	let clazz = '';
	export { clazz as class };

    let now = new Date(), month, day, year;
	let dateString;
	
	onMount(()=> {
        month = '' + (now.getMonth() + 1),
        day = '' + now.getDate(),
        year = now.getFullYear();

    if (month.length < 2) 
        month = '0' + month;
    if (day.length < 2) 
        day = '0' + day;

    dateString = [year, month, day].join('-');
	})


</script>



<div class="mb-4">
  <div class="flex mx-4 ">
    <label class='relative cursor-pointers my-4 {width}'>
      <input 
      bind:value={dateString}
      type="date"
      {disabled}
      {placeholder}
      class="
        w-full datepicker  h-[5rem] text-3xl border-gray-700 pt-4 pl-0 pr-6 border-b-2 focus:border-blue-500 border-opacity-50 outline-none placeholder-gray-300 placeholder-opacity-0 transition-colors duration-200 
        {variant}
      "
    />
    <span class='{variant}-label input-text left-0 top-6 transition duration-200 text-3xl font-medium text-gray-700 text-opacity-80 absolute'>{placeholder}</span>
    </label>
  </div>
  <span class="ml-4 text-xl text-gray-500">{helperText}</span>
</div>


<style>
  input[type="date"]:focus ~ .input-text,
  input[type="date"]:not(:placeholder-shown) ~ .input-text:focus{
	@apply text-blue-700 transform -translate-y-10 -translate-x-4 scale-75;
  }
  input[type="date"]:not(:placeholder-shown) ~ .input-text{
	@apply transform  -translate-y-10 -translate-x-4 scale-75;
  }
</style>