<script>
    import CheckBox from '$lib/ui/inputs/CheckBox.svelte'
	export let title;
	let clazz = '';
	export { clazz as class };

</script>


<table class="fsTable text-lg">
	<thead>
        <td><CheckBox /></td>
        <td>Header One</td>
        <td>Header Two</td>
        <td>Header Three</td>
	</thead>
	<tbody>
        <tr>
           <td><CheckBox /></td>
           <td>One</td>
            <td>Two</td>
            <td>Three</td>
        </tr>
	</tbody>
    <tbody>
        <tr>
           <td><CheckBox /></td>
           <td>One</td>
            <td>Two</td>
            <td>Three</td>
        </tr>
	</tbody>
</table>


<style>
.fsTable {
    border-radius: 5px;
    font-weight: normal;
    border: none;
    border-collapse: collapse;
    max-width: 100%;
    white-space: nowrap;
    background-color: white;
}
.fsTable thead td{
    font-weight: 500;
}
.fsTable td, .fsTable th {
    padding: 8px;
    border-bottom: 1px solid #e0e0e0;
    text-align: center;
}
.fsTable tr:last-child{
    border-bottom: 1px solid transparent ;
}
.fsTable tr:hover{
    background-color: #f1f1f1;
}
@media (max-width: 500px) {
    .fsTable {
        display: block;
        width: 100%;
    }
    .fsTable thead, .fsTable tbody, .fsTable thead th {
        display: block;
    }
    .fsTable thead th:last-child{
        border-bottom: none;
    }
    .fsTable thead {
        float: left;
    }
    .fsTable tbody {
        width: auto;
        position: relative;
        overflow-x: auto;
    }
    .fsTable td, .fsTable th {
        padding: 20px .625em .625em .625em;
        vertical-align: middle;
        box-sizing: border-box;
        overflow-x: hidden;
        overflow-y: auto;
        text-overflow: ellipsis;
    }
    .fsTable thead th {
        text-align: left;
        border-bottom: 1px solid #e0e0ee;
        border-right: 1px solid #e0e0ee;
    }
    .fsTable thead th:nth-child(odd) {
        background-color: #f8f8f8;
    }
    .fsTable tbody tr {
        display: table-cell;
    }
    .fsTable tbody tr:nth-child(odd) {
        background: none;
    }
    .fsTable tr:nth-child(even) {
        background: transparent;
    }
    .fsTable tr td:nth-child(odd) {
        background: #F8F8F8;
        border-right: 1px solid #E6E4E4;
    }
    .fsTable tr td:nth-child(even) {
        border-right: 1px solid #E6E4E4;
    }
    .fsTable tbody td {
        display: block;
    }
}
</style>