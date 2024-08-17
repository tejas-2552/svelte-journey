<script>
	let name = "Jhon Wick";
	let dogColor = "black";
	let color = '';
	const handleOnClick = () => {
		if(color !== ''){
			dogColor = color;
		} else {
			alert("Cannot be empty!");
		}
	}
	
	const handleInput = (e) =>
	{
		dogColor = e.target.value;
	}
</script>

<main>
	<h1>Hello {name}!</h1>
	<h2>Dog color : {dogColor}</h2>
	<button on:click={handleOnClick}>Click to update the dog color</button>
	<input type="text" bind:value={color}>
</main>

<style>
	main { 
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>