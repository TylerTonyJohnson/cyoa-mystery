<script>
	import '../styles.css';

	const story_words = [
		'You are outside, looking up at a large brick house as the sun sets behind it. The building is familiar, though you haven’t seen it for many years. All the windows are dark, save one. In an upstairs window, a single candle flickers, barely illuminating a face you recognize. The woman looks older than you remember, and her face is twisted in agony. Her gaze connects with yours, and her hand presses against the window, as though she is trying to reach for you. “Help me,” she mouths. The candle goes out. All around you, darkness presses in until you see nothing but black. ',

		'You open your eyes and sit up, realizing that it was a dream. Still, the image of your aunt’s face is imprinted on your mind, and you cannot shake the foreboding feeling in the pit of your stomach. '
	];

	let current_part = $state(0);

	function next_part() {
		current_part = (current_part + 1) % story_words.length;
	}
</script>

<!-- STRUCTURE -->

<div class="main">
	<div class="story-image">
		<div class="text-content">
			<p class="story-text" onclick={next_part}>
				{story_words[current_part]}
			</p>
		</div>
	</div>
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
		display: grid;
		grid-template-rows: 50% auto;
		grid-template-areas: '.' ' content';
		flex-direction: column; /* width: 100%; */
		height: 100%;
		aspect-ratio: 2/3;
		background-image:
			linear-gradient(to right, #000000, transparent, transparent, #000000),
			url('/images/opening scene.png');
		background-size: contain;
		background-repeat: no-repeat;
		background-position: center;
		/* border: solid 1px pink; */
	}
	.text-content {
		display: flex;
		justify-content: center;
		align-items: center;
		grid-area: content;
		/* border: solid 2px orange; */
	}
	.story-text {
		background-color: hsla(64, 35%, 92%, 0.35);
		padding: 3rem;
		font-family: 'ParagraphFont';
		font-size: 1.73rem;
		color: rgb(154, 149, 123);
		text-shadow: -2px 2px 2px black;
		text-align: center;
		line-height: 1.3;
		letter-spacing: 0.025rem;
		border: solid 12px rgb(39, 6, 6);
	}
</style>
