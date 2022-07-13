<script>
	export let caption;
	export let href = null;
	export let alt = '';
	export let leftIcon = null;
	export let rightIcon = null;
	export let processing = false;
	export let disabled = false;
	export let variant = '';
	export let color = '';
	let clz = '';
	export { clz as class };

	const defualtClass =
		'text-xl  py-4 px-10 m-2 font-medium text-center flex justify-center items-center';

	$: processingClass = processing ? 'bg-gray-400' : '';
	$: disabledClass = disabled ? 'text-gray-500' : '';
</script>

{#if href}
	<a
		{href}
		{alt}
		class="
			{defualtClass}
			{disabledClass}
			{processingClass}
			{clz}
		"
	>
		{#if leftIcon}
			<img src={leftIcon} alt="menu" class="h-8 mr-2" />
		{/if}
		{#if caption}
			{caption}
		{/if}
		{#if rightIcon}
			<img src={rightIcon} alt="menu" class="rotate-180 h-8 ml-2" />
		{/if}
	</a>
{:else}
	<button
		on:click
		disabled={processing || disabled}
		{alt}
		class="
		{defualtClass}
		{disabledClass}
		{processingClass}
		{clz}
		{variant}{color}
	"
	>
		{#if leftIcon && !processing}
			<img src={leftIcon} alt="menu" class="h-8 mr-2" />
		{/if}
		{#if caption}
			{caption}
		{/if}
		{#if rightIcon && !processing}
			<img src={rightIcon} alt="menu" class="h-8 ml-2" />
		{/if}
		{#if processing}
			<div class="ml-6">
				<Spinner />
			</div>
		{/if}
	</button>
{/if}
