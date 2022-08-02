<script>
	export let title;
	let clazz = '';
	export { clazz as class };

 

</script>


<table class="fsTable text-lg">
	<slot />
</table>



<style>
.fsTable {
    border-radius: 5px;
    font-weight: normal;
    border: none;
    border-collapse: collapse;
    width: 100%;
    max-width: 100%;
    white-space: nowrap;
    background-color: white;
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