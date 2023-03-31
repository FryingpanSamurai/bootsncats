<script>
	// need a year
	let d = new Date().getFullYear();
</script>

<style>
	:global(*) {
		padding: 0;
		margin: 0;
	}

	#main{
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		background-color: #555;
		height: 100vh;
		width: 100vw;
	}

	#bootsandcats {
		display: flex;
		gap: 30px;
	}

	#cathead {
		position: relative;
		height: 200px;
		top: -280px;
		left: 200px;
		width: auto;
	}

	#catbody {
		height: 400px;
		width: auto;
	}

	#boots {
		height: 400px;
	}

	#svelte-icon {
		position: relative;
		top: 8px;
		height: 25px;
	}

	footer {
		display: flex;
		justify-content: center;
		align-items: baseline;
		height: 40px;
		width: 100%;
		position: absolute;
		bottom: 0px;
		background-color: #333;
	}
</style>

<!-- ROOT DOC -->
<div id="main">
	<!-- boots and cat here -->
	<div id="bootsandcats">
		<img id="boots" src="rubberboots.svg">
		<div id="cat">
			<img id="cathead" src="catface-color.svg">
			<img id="catbody" src="catsil.svg">
		</div>
	</div>
	<!-- boot icon and cat icon font-awesome -->
	<div id="bnc-icon">
		<i class="fas fa-socks"></i>
		<i class="fas fa-xs fa-plus"></i>
		<i class="fas fa-cat"></i>
	</div>
	<!-- footer -->
	<footer>
		<span>
			&copy; {d} - arb1z websites 
			<img id="svelte-icon" src="svelte-logo.svg">
		</span>
	</footer>
</div>
