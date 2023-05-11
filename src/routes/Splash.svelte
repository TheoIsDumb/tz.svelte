<script>
    import { fade } from 'svelte/transition';
    let visible = true;
</script>

{#if visible}
    <div class="splash" transition:fade={{duration: 1000}}>
        <div style:text-align=center>
            <h1 style:font-size=3rem>tz.vkdbois.xyz</h1>
            <p>sift through timezones.</p>
            <span>made with svelte.</span>
        </div>

        <button on:click={() => visible = !visible}>Click to start</button>
    </div>
{/if}

<style>
    div.splash {
        position: fixed;
        background-color: rgba(0,0,0,0.8);
        color: #fff;
        height: 100dvh;
        width: 100%;
        top: 0;
        left: 0;
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 5rem;
        flex-direction: column;
    }

    h1, p {
        margin: 0;
    }
</style>