<script>
    import {fade} from 'svelte/transition';

    let text = "";
    let animate = false;

    function handleInputChange(event){
        animate = !animate;
        setTimeout(() => {animate = true;}, 250)
    }
</script>

<div>
    <input bind:value={text} on:input={handleInputChange} placeholder="Enter text here." type="text" id="input_text" name="input_text">
    {#if animate}
        <p transition:fade >
            {text}
        </p>
    {/if}
</div>

<style>

</style>