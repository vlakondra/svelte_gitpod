<script>
    export let text;
    export let funccount;
</script>

<div>
    {text} компонент
    <div>
        <button on:click={funccount}>counter</button>
    </div>
</div>

<style>
    div{
        color:red;
    }
</style>
