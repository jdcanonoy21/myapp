<script>
	import TextField from "$lib/ui/inputs/TextField.svelte";
	import Container from "$lib/ui/Container.svelte";
	import Paper from "$lib/ui/Paper.svelte";
	import Button from "$lib/ui/inputs/Button.svelte";
	import Radio from "$lib/ui/inputs/Radio.svelte";
	import Select from "$lib/ui/inputs/Select.svelte";
	import MenuItem from "$lib/ui/inputs/MenuItem.svelte";
	import CheckBox from "$lib/ui/inputs/CheckBox.svelte";
	import RadioGroup from "$lib/ui/RadioGroup.svelte";
	import Datefield from "$lib/ui/DesktopDatePicker.svelte";
	import Drawer from "$lib/ui/navigation/Drawer.svelte";
	import Table from "$lib/ui/datadisplay/Table.svelte";
	import DataTable from "$lib/ui/datadisplay/DataTable.svelte";
	import TableHeader from "$lib/ui/datadisplay/TableHeader.svelte";
	import TableBody from "$lib/ui/datadisplay/TableBody.svelte";
	import TableRow from "$lib/ui/datadisplay/TableRow.svelte";
	import TableCell from "$lib/ui/datadisplay/TableCell.svelte";
	import MaskedTextField from "$lib/ui/inputs/MaskedTextField.svelte";
	import "../style.css"
</script>

<Container>
	<Paper>
		<div class="p-10">
			<TextField  placeholder="Email Address" variant="standard" width="full" helperText="Some important text"/>
			<TextField  placeholder="Mobile No." variant="standard" width="full"/>
			<div class="flex justify-between mt-16 pt-10 border-t-2">
				<Button caption="Back" color="primary" />
				<Button caption="Submit" variant="contained" color="primary" />
			</div>
		</div>
	</Paper>
	<Paper>
		<h1 class="mb-6 border-b-2 text-2xl pl-4">Contained Buttons</h1>
		<div class="flex mb-8">
			<Button caption="Default" variant="contained" />
			<Button caption="Primary" variant="contained" color="primary" />
			<Button caption="Secondary" variant="contained" color="secondary" />
			<Button caption="Disabled" variant="contained" disabled />
		</div>
		<h1 class="mb-6 border-b-2 text-2xl pl-4">Text Buttons</h1>
		<div class="flex mb-8 pl-4 pb-4">
			<Button caption="Default" color="default" />
			<Button caption="Primary" color="primary" />
			<Button caption="Secondary" color="secondary" />
			<Button caption="Disabled" disabled />
		</div>
		<h1 class="mb-6 border-b-2 text-2xl pl-4">Outline Buttons</h1>
		<div class="flex mb-8 pl-4 pb-4">
			<Button caption="Default" variant="outlined" />
			<Button caption="Primary" variant="outlined" color="primary" />
			<Button caption="Secondary" variant="outlined" color="secondary" />
			<Button caption="Disabled" variant="outlined" disabled />
		</div>
	</Paper>
	<Paper>
		<h1 class="mb-6 border-b-2 text-2xl pl-4">TextField</h1>
		<div class="flex mb-8 pl-4 pb-4">
			<TextField placeholder="Standard" variant="standard"/>
		</div>
	</Paper>
	<Paper>
		<h1 class="mb-6 border-b-2 text-2xl pl-4">Basic Radio</h1>
		<div class="mb-8 pl-4 pb-4">
			<div class="flex mb-9">
				<Radio checked/>
				<Radio />
				<Radio disabled checked/>
				<Radio disabled/>
			</div>
		</div>
		<h1 class="mb-6 border-b-2 text-2xl pl-4">Radio Group</h1>
		<div class="mb-8 pl-4 pb-4">
			<RadioGroup>
				<Radio name="gender" label="Male" checked/>
				<Radio name="gender" label="Female"/>
				<Radio name="gender" label="others" disabled/>
			</RadioGroup>
		</div>
		<h1 class="mb-6 border-b-2 text-2xl pl-4">Radio Color</h1>
		<div class="mb-8 pl-4 pb-4">
			<RadioGroup>
				<Radio label="Primary" checked/>
				<Radio label="Secondary" checked color="secondary"/>
				<Radio label="Success" checked color="success"/>
			</RadioGroup>
		</div>
	</Paper>
	<Paper>
		<h1 class="mb-6 border-b-2 text-2xl pl-4">Basic Checkbox</h1>
		<div class="mb-8 pl-4 pb-4">
			<div class="flex mb-9">
				<CheckBox checked/>
				<CheckBox />
				<CheckBox disabled/>
				<CheckBox disabled checked/>
			</div>
		</div>
		<h1 class="mb-6 border-b-2 text-2xl pl-4">Color Checkbox</h1>
		<div class="mb-8 pl-4 pb-4">
			<div class="flex mb-9">
				<CheckBox label="Primary" checked color="primary"/>
				<CheckBox label="Secondary" checked color="secondary"/>
				<CheckBox label="Success" checked color="success"/>
			</div>
		</div>
		<h1 class="mb-6 border-b-2 text-2xl pl-4">Size Checkbox</h1>
		<div class="mb-8 pl-4 pb-4">
			<div class="flex mb-9">
				<CheckBox checked/>
				<CheckBox />
				<CheckBox disabled/>
				<CheckBox disabled checked/>
			</div>
		</div>
	</Paper>
	<Paper>
		<h1 class="mb-6 border-b-2 text-2xl pl-4">Select</h1>
		<div class="mb-8 pl-4 pb-4">
			<Select placeholder="Select Standard" width="full">
				<MenuItem value="2" label="Option 1"/>
				<MenuItem value="3" label="Option 2"/>
			</Select>
		</div>
	</Paper>
	<Paper>
		<h1 class="mb-6 border-b-2 text-2xl pl-4">Datefield</h1>
		<div class="mb-8">
			<Datefield  placeholder="Date Desktop"/>
		</div>
	</Paper>
	<Paper>
		<Table>
			<TableHeader>
				<TableRow>
					<TableCell>Header 1</TableCell>
					<TableCell textAlign="right">Header 2</TableCell>
					<TableCell textAlign="right">Header 3</TableCell>
					<TableCell textAlign="right">Header 4</TableCell>
				</TableRow>
			</TableHeader>
			<TableBody>
				<TableRow>
					<TableCell>content1</TableCell>
					<TableCell textAlign="right">content 2</TableCell>
					<TableCell textAlign="right">content 3</TableCell>
					<TableCell textAlign="right">content 4</TableCell>
				</TableRow>
				<TableRow>
					<TableCell>content1</TableCell>
					<TableCell textAlign="right">content 2</TableCell>
					<TableCell textAlign="right">content 3</TableCell>
					<TableCell textAlign="right">content 4</TableCell>
				</TableRow>
			</TableBody>
		</Table>
	</Paper>
	<Paper>
		<DataTable />
	</Paper>
</Container>


