<script>
	import {onMount} from 'svelte';
	// need a year
	let d = new Date().getFullYear();
</script>

<style>
	:global(*) {
		padding: 0;
		margin: 0;
	}

	@keyframes headbobleft {
		from {
			top: 27%;
			left: 50%;
		}
		to {
			top: 29%;
			left: 48%;
		}
	}

	@keyframes bootsbob {
		from {
			transform: scaleX(1);
		}
		to {
			transform: scaleX(-1);
		}
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
		width: 100%;
		display: flex;
		justify-content: space-evenly;
		padding-bottom: 100px;
	}

	#cat {
		height: 200px;
		object-fit: contain;
	}

	#cathead {
		position: absolute;
		height: 75px;
		width: auto;
		animation: headbobleft 0.25s infinite;
		animation-direction: alternate;
	}

	#catbody {
		height: 200px;
		width: auto;
	}

	#boots {
		height: 200px;
		object-fit: contain;
		animation: bootsbob 0.5s infinite linear;
		animation-direction: alternate;
	}

	#bnc-icon {
		font-size: xxx-large;
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
		font-family: "Tahoma";
	}

	@media only screen and (min-width: 768px) {
		/* design for desktop */
		#cathead {
			height: 150px;
		}

		#catbody {
			height:400px;
		}

		@keyframes headbobleft {
			from {
				top: 27%;
				left: 57%;
			}
			to {
				top: 28%;
				left: 55%;
			}
		}
	}
</style>

<!-- ROOT DOC -->
<div id="main">
	<!-- boots and cat here -->
	<div id="bootsandcats">
		<img alt="boots" id="boots" src="rubberboots.svg">
		<div id="cat">
			<img
				alt="cat head"
				id="cathead" 
				src="catface-color.svg">
			<img alt="cat body" id="catbody" src="catsil.svg">
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
			&copy; {d} - arb1z websites' 
			<img alt="svelte icon" id="svelte-icon" src="svelte-logo.svg">
		</span>
	</footer>
</div>
