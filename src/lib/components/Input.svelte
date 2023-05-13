<script>
    export let searchquery;
</script>

<div class="input">
    <input type="text" bind:value={searchquery} placeholder="Search..."/>
    <input type="button" on:click={() => {searchquery = ""}} value="✕">
</div>

<style>
    div.input {
        display: grid;
        grid-template-columns: 8fr 1fr;
        grid-gap: 0.5rem;
        height: 8%;
        border-bottom-left-radius: inherit;
        border-top: 2px solid gray;
    }
    input[type="text"] {
        background-color: black;
        color: white;
        border-bottom-left-radius: inherit;
        border: 0;
        padding: 0.5rem;
    }
    input[type="button"] {
        background-color: transparent;
        color: white;
        border: 0;
    }
</style>