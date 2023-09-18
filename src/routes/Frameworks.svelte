<script>
    import NoiseBg from '$lib/images/noiseFrameworks.png'
</script>

<div class="framework">
	<div class="headingText">
		<div class="italic">Frameworks
			<div class="underline"></div>
		</div>
	</div>
	<h2 class="description">Swiftly power. plus even more power!</h2>

    <img src={NoiseBg} alt="backgrond" class="noiseBg">
</div>

<style>	
	@import url('https://fonts.googleapis.com/css2?family=Source+Sans+3:wght@200;300;400;500;600;700;800;900&display=swap');

    .framework{
        margin-top: 12rem;
    }

	.headingText{
		position: relative;
		align-items: center;
		justify-content: center;
		display: flex;
		top: 1rem;
	}

	.italic {
		text-align: center;
		font-family: "saolDisplay";
		font-size: 80px;
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
		width: 420px;
		height: 15px;
		background: linear-gradient(97deg, #00C9FF 0%, #92FE9D 100%);
		position: absolute; /* Position the underline absolutely within the "Swiftly" text */
		bottom: 22px; /* Adjust this as needed to position the underline below the text */
		left: -15px; /* Center the underline */
		z-index: -1;
	}

	.description {
		color: #444;
		margin-top: 1.5rem;
		font-family: 'Switzer';
		font-size: 21px;
		font-style: normal;
		font-weight: 400;
		line-height: normal;
		text-align: center;
	}

    .noiseBg{
        position: absolute;
        left: 50%;
        transform: translateX(-50%);
        width: 50%;
        z-index: -1;
    }

	@media only screen and (max-width: 750px){
		.italic{
			font-size: 4rem;
		}

		.underline{
			width: 330px;
			margin-left: 0.5rem;
            bottom: 10px;
			height: 15px;
		}

		.headingText{
			margin-top: 1rem;
			gap: 1.5rem;
		}

		.description{
			margin-top: 1rem;
			font-size: 1.2rem;
			padding: 0 1rem;
		}
	}
	
	@media only screen and (max-width: 550px){
		.italic{
			font-size: 3.5rem;
		}

		.underline{
			width: 290px;
			margin-left: 0.5rem;
			height: 15px;
		}

		.headingText{
			margin-top: 1rem;
			gap: 1.3rem;
		}

		.description{
			margin-top: 1rem;
			font-size: 1.1rem;
			padding: 0 1rem;
		}
	}
	
	@media only screen and (max-width: 425px){
		.italic{
			font-size: 3rem;
		}

		.underline{
			width: 240px;
			margin-left: 0.7rem;
			height: 10px;
			bottom: 8px;
		}

		.headingText{
			margin-top: 1rem;
			gap: 0.9rem;
		}

		.description{
			margin-top: 1.5rem;
			font-size: 1.1rem;
			padding: 0 1rem;
		}
	}

	@media only screen and (max-width: 375px){
		.italic{
			font-size: 3rem;
		}

		.underline{
			width: 240px;
			margin-left: 0.7rem;
			height: 10px;
			bottom: 12px;
		}

		.headingText{
			margin-top: 1rem;
			gap: 0.9rem;
		}

		.description{
			margin-top: 1.5rem;
			font-size: 1.1rem;
			padding: 0 1rem;
		}

		.magic{
			left: 36%;
		}
	}
</style>
