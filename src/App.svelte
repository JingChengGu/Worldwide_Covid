<script>
	//export let name = 'World';
	import WorldMap from './WorldMap.svelte';
	let daysCount;
  </script>
  
  <main>
	<h1>WorldWide Covid Data</h1>
	<p>A Visualizaiton of how covid took over the world, here is the data we used <a href="https://www.kaggle.com/datasets/imdevskp/corona-virus-report?resource=download">Covid Data</a>.</p>
	<input type="range" min="0" max="daysCount" value="0" id="timeSlider" step="1">
	<label for="timeSlider" id="sliderLabel">Date: </label>
	<WorldMap/>
  </main>
  
<style>
	@import url('https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@0;1&family=Oswald:wght@200..700&family=Rubik:ital,wght@0,300..900;1,300..900&display=swap');

	main {
		text-align: center;
		padding: 1em;
		width: 100%;
		margin: 0 auto;
		font-family: 'Rubik', sans-serif; /* Change the font-family as needed */
	}

	h1 {
		color: #4b0000;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 3000;
		font-family: 'DM Serif Display', serif; /* Change the font-family as needed */
	}

	p {
		font-family: 'Oswald', sans-serif; /* Change the font-family as needed */
		font-size: 1.3em; /* Adjust the size as needed */
	}

	#timeSlider {
        background: linear-gradient(to right, #ddd 0%, #ddd 100%); 
        width: 50%; 
        border-radius: 10px; 
    }

    #timeSlider::-moz-range-track {
        width: 100%;
        height: 8px;
        background: #ffffff;
        border-radius: 10px;
    }
    #timeSlider::-webkit-slider-thumb {
        transition: background-color 0.3s ease-in-out;
        transform: translate3d(0, 0, 0);
    }
    #timeSlider::-moz-range-thumb {
          transition: background-color 0.3s ease-in-out;
        transform: translate3d(0, 0, 0);
    }
    #sliderLabel {
        display: block;
        margin-top: 10px; 
        font-size: 1.1em;
        color: #333;
    }
</style>
