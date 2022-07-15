<script>
	import TextField from "$lib/ui/TextField.svelte";
	import Container from "$lib/ui/Container.svelte";
	import Paper from "$lib/ui/Paper.svelte";
	import Button from "$lib/ui/Button.svelte";
	import Radio from "$lib/ui/Radio.svelte";
	import Select from "$lib/ui/Select.svelte";
	import MenuItem from "$lib/ui/MenuItem.svelte";
	import CheckBox from "$lib/ui/CheckBox.svelte";
	import RadioGroup from "$lib/ui/RadioGroup.svelte";
	import Datefield from "$lib/ui/DesktopDatePicker.svelte";
	import "../style.css"
</script>

<Container>
	<Paper>
		<TextField  placeholder="Email Address" variant="standard" width="full" helperText="Some important text"/>
		<TextField  placeholder="Mobile No." variant="standard" width="full"/>
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
	<Paper>
		<h1 class="mb-6 border-b-2 text-2xl">Basic Radio</h1>
		<div class="mb-8">
			<div class="flex mb-9">
				<Radio checked/>
				<Radio />
				<Radio disabled checked/>
				<Radio disabled/>
			</div>
		</div>
		<h1 class="mb-6 border-b-2 text-2xl">Radio Group</h1>
		<div class="mb-8">
			<RadioGroup>
				<Radio name="gender" label="Male" checked/>
				<Radio name="gender" label="Female"/>
				<Radio name="gender" label="others" disabled/>
			</RadioGroup>
		</div>
		<h1 class="mb-6 border-b-2 text-2xl">Radio Color</h1>
		<div class="mb-8">
			<RadioGroup>
				<Radio label="Primary" checked/>
				<Radio label="Secondary" checked color="secondary"/>
				<Radio label="Success" checked color="success"/>
			</RadioGroup>
		</div>
	</Paper>
	<Paper>
		<h1 class="mb-6 border-b-2 text-2xl">Basic Checkbox</h1>
		<div class="mb-8">
			<div class="flex mb-9">
				<CheckBox checked/>
				<CheckBox />
				<CheckBox disabled/>
				<CheckBox disabled checked/>
			</div>
		</div>
		<h1 class="mb-6 border-b-2 text-2xl">Color Checkbox</h1>
		<div class="mb-8">
			<div class="flex mb-9">
				<CheckBox label="Primary" checked color="primary"/>
				<CheckBox label="Secondary" checked color="secondary"/>
				<CheckBox label="Success" checked color="success"/>
			</div>
		</div>
		<h1 class="mb-6 border-b-2 text-2xl">Size Checkbox</h1>
		<div class="mb-8">
			<div class="flex mb-9">
				<CheckBox checked/>
				<CheckBox />
				<CheckBox disabled/>
				<CheckBox disabled checked/>
			</div>
		</div>
	</Paper>
	<Paper>
		<h1 class="mb-6 border-b-2 text-2xl">Select</h1>
		<div class="mb-8">
			<Select placeholder="Select Standard" width="full">
				<MenuItem value="2" label="Option 1"/>
				<MenuItem value="3" label="Option 2"/>
			</Select>
			<Select variant="outlined" placeholder="Select Outlined" width="50">
				<MenuItem value="1" label="Option 1"/>
				<MenuItem value="2" label="Option 2"/>
				<MenuItem value="3" label="Option 3"/>
			</Select>
		</div>
	</Paper>
	<Paper>
		<h1 class="mb-6 border-b-2 text-2xl">Datefield</h1>
		<div class="mb-8">
			<Datefield  placeholder="Date Desktop"/>
			<Datefield placeholder="Outlined" variant="outlined"/>
			
		</div>
	</Paper>
</Container>


