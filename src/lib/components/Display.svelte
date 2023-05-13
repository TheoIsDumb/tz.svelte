<script>
    export let date = "--------";
    export let time = "--:--:--";
    export let timezone = "----------";
</script>

<div>
    <h2>{date}</h2>
    <h1 style:font-size=4rem>{time}</h1>
    <p>{timezone}</p>
</div>

<style>
    div {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        height: 40%;
    }
    h1,h2,p {
        margin: 0;
    }
</style>