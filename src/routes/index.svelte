<script>
	import TextField from "$lib/ui/TextField.svelte";
	import Container from "$lib/ui/Container.svelte";
	import Paper from "$lib/ui/Paper.svelte";
	import Button from "$lib/ui/Button.svelte";
	import "../style.css"
</script>

<Container>
	<Paper>
		<TextField  placeholder="Email Address" variant="standard"/>
		<TextField  placeholder="Mobile No." variant="standard"/>
		<div class="flex justify-between mt-16 pt-10 border-t-2">
			<Button caption="Back" color="primary" />
			<Button caption="Submit" variant="contained" color="primary" />
		</div>
	</Paper>
	<Paper>
		<h1 class="mb-6 border-b-2 text-2xl">Contained Buttons</h1>
		<div class="flex mb-8">
			<Button caption="Default" variant="contained" />
			<Button caption="Primary" variant="contained" color="primary" />
			<Button caption="Secondary" variant="contained" color="secondary" />
			<Button caption="Disabled" variant="contained" disabled />

		</div>
		<h1 class="mb-6 border-b-2 text-2xl">Text Buttons</h1>
		<div class="flex mb-8">
			<Button caption="Default" color="default" />
			<Button caption="Primary" color="primary" />
			<Button caption="Secondary" color="secondary" />
			<Button caption="Disabled" disabled />
		</div>
		<h1 class="mb-6 border-b-2 text-2xl">Outline Buttons</h1>
		<div class="flex mb-8">
			<Button caption="Default" variant="outlined" />
			<Button caption="Primary" variant="outlined" color="primary" />
			<Button caption="Secondary" variant="outlined" color="secondary" />
			<Button caption="Disabled" variant="outlined" disabled />
		</div>
	</Paper>
	<Paper>
		<h1 class="mb-6 border-b-2 text-2xl">TextField</h1>
		<div class="flex mb-8">
			<TextField placeholder="Standard" variant="standard"/>
			<TextField placeholder="Filled"  variant="filled"/>
			<TextField placeholder="Outline" variant="outlined"/>
		</div>
		<h1 class="mb-6 border-b-2 text-2xl">Form props</h1>
		<div class="flex mb-8">
			<TextField placeholder="Required" variant="standard" value="Jason Delle" type="text"/>
			<TextField placeholder="Password"  variant="standard" type="password"/>
			<TextField placeholder="Outline" variant="outlined"/>
		</div>
	</Paper>
</Container>


