<script>
	export let value;
	export let placeholder = '';
	export let disabled = false;
  export let color='';
  export let width='';
  export let helperText='';
  export let variant='';
	let clazz = '';
	export { clazz as class };

	let inputRef;

	export const focus = () => {
		if (inputRef) inputRef.focus();
	};


</script>

<div class="mb-4">
  <div class="flex justify-center items-center mx-4 ">
    <label class='relative cursor-pointers my-4 {width}'>
      <input 
      bind:this={inputRef}
      bind:value
      type="text"
      {disabled}
      {placeholder}
      class="
        w-full  h-[5rem] pl-4 text-2xl border-gray-700 border-b-2 focus:border-blue-500 focus:border-b-4 border-opacity-50 outline-none placeholder-gray-300 placeholder-opacity-0 transition-colors duration-200 hover:border-b-4 hover:border-gray-700
        {variant}
      "
    />
      <span class='{variant}-label input-text transition duration-200 text-2xl font-medium text-gray-700 text-opacity-80 absolute'>{placeholder}</span>
    </label>
  </div>
  <span class="ml-4 text-xl text-gray-500">{helperText}</span>
</div>


<style>
  input[type="text"]:focus ~ .input-text,
  input[type="text"]:not(:placeholder-shown) ~ .input-text:focus{
	@apply text-blue-700 transform -translate-y-10 -translate-x-4 scale-75;
  }
  input[type="text"]:not(:placeholder-shown) ~ .input-text{
	@apply transform  -translate-y-10 -translate-x-4 scale-75;
  }
</style>