<script>
    export let textAlign='';
</script>

<td class="{textAlign}">
   <slot />
</td>

<style>
    td{
    padding: 16px;
    border-bottom: 1px solid #e0e0e0;
}
.right{
    text-align: right;
}
.left{
    text-align: left;
}
.center{
    text-align: center;
}
</style>