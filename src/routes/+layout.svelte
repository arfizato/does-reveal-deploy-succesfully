<script>
	import '../app.postcss';
</script>

<div class="container">
	<div class="navbar">
		<ul>
			<div><a href="#/0">1</a></div>
			<div><a href="#/1">2</a></div>
			<div><a href="#/2">3</a></div>
			<div><a href="#/3">4</a></div>
			<div><a href="#/4">5</a></div>

		</ul>
	</div>
	<slot />

</div>

<style>
	.container {
		margin: none;
		display: flex;
		height: 100vh;
		width: 100vw;
		border: #fff 2px solid;
	}

	.navbar {
		grid-area: navbar;
		/* background-color: #333; */
		color: #fff;
		border-right: #fff 2px solid;
		width: 200px;
		height: 100%;


	}
	.navbar ul {
		height: 100%;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: space-evenly;
	}

</style>