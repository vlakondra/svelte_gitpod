<script>
    export let text;
    export let funccount;
</script>


<div class="comp-one">
    {text} компонент
    <div>
        <button on:click={funccount}>counter</button>
    </div>
</div>

<style>
    .comp-one{
        border: 1px solid green;
        color:red;
    }
</style>
