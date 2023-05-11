<script>
    import Display from "./Display.svelte";
    import List from "./List.svelte";
    import { onMount } from "svelte";

    let timezone;
    let time;
    let date;

    onMount(() => {
    const interval = setInterval(() => {
        time = new Date().toLocaleTimeString('en-US', {
            timeZone: timezone,
            hour12: false
            },
        )
        date = new Date().toLocaleDateString('en-US', {
            timeZone: timezone,
            year: 'numeric', month: 'long', day: 'numeric'
        }
        );
    }, 1000);

    return () => {
			clearInterval(interval);
		};
    })
</script>

<style>
    div {
        display: flex;
        flex-direction: column;
        height: 70vh;
        width: 90%;
        max-width: 500px;
        border: 2px solid white;
        border-radius: 1rem;
    }
</style>

<div>
    <Display {time} {date} {timezone}/>
    <List bind:timezone={timezone}/>
</div>