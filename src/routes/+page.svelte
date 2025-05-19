<script>
</script>

<!-- STRUCTURE -->

<div class="main">
	<!-- <img src="images/opening scene.png" class="story-image"/> -->
	<div class="story-image"></div>
</div>

<!-- STYLES -->

<style>
	:global(*) {
		margin: 0;
		padding: 0;
		box-sizing: border-box;
	}

	.main {
		background-color: #000000;
		padding: 10px;
		width: 100vw;
		height: 100vh;
		overflow: hidden;
		display: flex;
		/* place-items: center; */
		place-content: center;
	}
	.story-image {
		background-color: black;
		/* width: 100%; */
		height: 100%;
		aspect-ratio: 2/3;
		background-image:
			linear-gradient(to right, #000000, transparent, transparent, #000000),
			url('/images/opening scene.png');
		background-size: contain;
		background-repeat: no-repeat;
		background-position: center;
	} 
</style>
