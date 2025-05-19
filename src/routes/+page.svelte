<script>
	let phone_no = 7852120554;

	let total = 0;

	// addItUp(phone_no);

	// console.log(total);

	// --- FUNCTIONS ---

	function addItUp() {
		let existing_value = 0;

		for (let i = 0; i < 10; i++) {
			// Transform phone number into a string
			const string_phone_no = phone_no.toString();

			//Get the current digit
			const current_digit = string_phone_no.charAt(i);

			// Turn current digit back into a number
			const current_digit_number = parseInt(current_digit);

			// console.log(current_digit_number);

			//Add the current digit to existing value
			existing_value = existing_value + current_digit_number;
		}

		total = existing_value;
		// return existing_value;
	}
</script>

<!-- STRUCTURE -->

<div class='main'>
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
background-image: linear-gradient(to right, #000000, transparent, transparent, #000000), url('images/opening scene.png');
background-size: contain;
background-repeat: no-repeat;
background-position: center;

}


	h2,
	h1 {
		color: white;
	}

	.special {
		color: blue;
		font-size: 2em;
		font-family: 'Courier New', Courier, monospace;
	}
</style>
