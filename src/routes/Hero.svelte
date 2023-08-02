<script>
    import winky from '$lib/images/winky.png';
    import magic from '$lib/images/magicSvg.svg';
    import copy from '$lib/images/copyIcon.svg';
    import Toastify from 'toastify-js'
    import 'toastify-js/src/toastify.css'

    function copyToClipboard() {
        navigator.clipboard.writeText('pip install swiftly-sys');
        Toastify({
            text: "Copied to clipboard!",
            duration: 3000
        }).showToast();
    }
</script>

<div class="heroSection">
	<div class="headingText">
		<div class="work">Work</div>
		<div class="swiftly">Swiftly
			<div class="underline"></div>
		</div>
	</div>
	<h2 class="goodAt">Do what you’re good at; writing code. Swiftly handles the rest <img class="winky" src={winky} alt="winking emoji"></h2>

	<img src={magic} alt="experience the magic" class="magic">

	<div class="copyDiv">
		<span class="copyText">pip install swiftly-sys</span>
		<div class="copyIcon" on:click={copyToClipboard}>
			<img src={copy} alt="copy icon">
		</div>
	</div>
</div>

<style>	
	@import url('https://fonts.googleapis.com/css2?family=Source+Sans+3:wght@200;300;400;500;600;700;800;900&display=swap');

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
		font-size: 120px;
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
		font-size: 120px;
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
		width: 340px;
		height: 20px;
		background: linear-gradient(97deg, #00C9FF 0%, #92FE9D 100%);
		position: absolute; /* Position the underline absolutely within the "Swiftly" text */
		bottom: 22px; /* Adjust this as needed to position the underline below the text */
		left: -15px; /* Center the underline */
		z-index: -1;
	}

	.goodAt {
		color: #444;
		margin-top: 1.5rem;
		font-family: 'Switzer';
		font-size: 21px;
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

	.copyDiv {
		position: relative;
		transform: translateX(-50%);
		border-radius: 10px;
		left: 50%;
		margin-top: 5rem;
		display: flex;
		justify-content: space-between;
		width: 17rem;
		font-family: 'Source Sans 3';
		align-items: center;
		background-color: #fff;
		border: 1.5px solid #B9B9BB;
		padding: 12px 18px;
		font-size: 18px;
	}

	.copyIcon{
		background: #E8E8E8;
		cursor: pointer;
		position: absolute;
		right: 0;
		top: 0;
		bottom: 0;
		width: 50px; /* Adjust this to change the width of the icon area */
		display: flex;
		align-items: center;
		justify-content: center;
		border-top-right-radius: 10px;
		border-bottom-right-radius: 10px;
	}

	.magic{
		position: absolute;
		left: 46.5%;
		transform: translateX(-50%);
	}	
</style>
