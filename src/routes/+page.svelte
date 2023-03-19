<script>
	let url = "/sites.json"
	import fetchStore from '../lib/scripts/fetch'
	const [data, loading, error, get] = fetchStore(url)

    function openRandomLink() {
        var link = $data[Math.floor(Math.random()*$data.length)];
        window.open(link, "_blank");
    }
</script>

<div class="container">
    <h1>Coywolf Surf</h1>
    <p>Discover the web all over again!</p>
    <button on:click|preventDefault={openRandomLink}>Suprise Me!</button>
    <a href="https://coywolf.com/surf/">Suggest a Site!</a>
</div>

<style>

    .container {
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: column;
        width: 100vw;
        height: 100vh;
    }

    .container h1 {
        
    }

</style>