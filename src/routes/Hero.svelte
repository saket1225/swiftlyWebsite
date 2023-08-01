<script>
    import winky from '$lib/images/winky.png';
	import magic from '$lib/images/magicSvg.svg'
</script>

<div class="heroSection">
	<div class="headingText">
		<div class="work">Work</div>
		<div class="swiftly">Swiftly
			<div class="underline"></div>
		</div>
	</div>
	<h2 class="goodAt">Do what you’re good at; writing code. Swiftly handle the rest <img class="winky" src={winky} alt="winking emoji"></h2>

	<!-- <img src={magic} alt="experience the magic" class="magic"> -->
</div>

<style>
	.headingText{
		position: relative;
		align-items: center;
		justify-content: center;
		display: flex;
		gap: 2rem;
		top: 1rem;
	}

	.work {
		text-align: center;
		font-family: "switzer";
		font-size: 130px;
		font-style: normal;
		font-weight: 900;
		line-height: normal;
		background: linear-gradient(180deg, #2C5364 0%, #203A43 50.52%, #0F2027 100%);
		background-clip: text;
		-webkit-background-clip: text;
		-webkit-text-fill-color: transparent;
  	}

	.swiftly {
		text-align: center;
		font-family: "saolDisplay";
		font-size: 130px;
		font-style: italic;
		font-weight: 300;
		line-height: normal;
		background: linear-gradient(180deg, #2C5364 0%, #203A43 50.52%, #0F2027 100%);
		background-clip: text;
		-webkit-background-clip: text;
		-webkit-text-fill-color: transparent;
		position: relative; /* Add this to position the underline relative to the "Swiftly" text */
	}

	.underline {
		width: 350px;
		height: 20px;
		background: linear-gradient(97deg, #00C9FF 0%, #92FE9D 100%);
		position: absolute; /* Position the underline absolutely within the "Swiftly" text */
		bottom: 22px; /* Adjust this as needed to position the underline below the text */
		left: -10px; /* Center the underline */
		z-index: -1;
	}

	.goodAt {
		color: #444;
		margin-top: 2rem;
		font-family: 'Switzer';
		font-size: 23px;
		font-style: normal;
		font-weight: 400;
		line-height: normal;
		text-align: center;
	}

	.winky{
		position: relative;
		bottom: -2.5px;
		left: 2px;
		width: 24px;	
	}

	
</style>
