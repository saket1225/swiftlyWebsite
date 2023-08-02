<script>
    import { currentOs } from './store.js';
    import { onMount } from 'svelte';
    import logo from '$lib/images/swiftly-logo.png';
    import apple from '$lib/images/appleActive.png'
    import linux from '$lib/images/linuxActive.png'
    import windows from '$lib/images/windowsActive.png'
    import heroBg from '$lib/images/heroBgNoise.png'

    onMount(() => {
        function getOperatingSystem() {
            var userAgent = window.navigator.userAgent,
                platform = window.navigator.platform,
                macosPlatforms = ['Macintosh', 'MacIntel', 'MacPPC', 'Mac68K'],
                windowsPlatforms = ['Win32', 'Win64', 'Windows', 'WinCE'],
                iosPlatforms = ['iPhone', 'iPad', 'iPod'],
                os = null;

            if (macosPlatforms.indexOf(platform) !== -1) {
                os = 'mac';
            } else if (iosPlatforms.indexOf(platform) !== -1) {
                os = 'mac';
            } else if (windowsPlatforms.indexOf(platform) !== -1) {
                os = 'windows';
            } else if (/Android/.test(userAgent)) {
                os = 'windows';
            } else if (!os && /Linux/.test(platform)) {
                os = 'linux';
            }

            return os;
        }

        console.log(getOperatingSystem());

        currentOs.set(getOperatingSystem());
    })

    function setOs(os) {
        currentOs.set(os);
    }
</script>

<header>
    <div class="nav-left">
        <a href="./">
            <img src={logo} alt="Swiftly Logo" class="logo">
            <h2 class="logoText">Swiftly</h2>
        </a>
    </div>
    <div class="nav-right">
        <img class="platforms apple {$currentOs === 'mac' ? 'active' : ''}" src={apple} alt="Apple platforms" on:click={() => setOs('mac')}>
        <img class="platforms linux {$currentOs === 'linux' ? 'active' : ''}" src={linux} alt="Linux platforms" on:click={() => setOs('linux')}>
        <img class="platforms windows {$currentOs === 'windows' ? 'active' : ''}" src={windows} alt="Windows platforms" on:click={() => setOs('windows')}>
    </div>
</header>

<img src={heroBg} alt="Hero background" class="heroBg">

<style>
	.heroBg{
		position: absolute;
		inset: 0;
		z-index: -100;
		width: 100%;
		height: 100%;
	}

	header {
		position: sticky;
		inset: 0;
		display: flex;
		justify-content: space-between;
		align-items: center;
		background-color: rgba(255, 255, 255, 0.3);
		backdrop-filter: blur(4px);
		height: 4rem;
		border-bottom: 1px solid #B9B9BB;
	}

	.nav-left a{
		display: flex;
		flex-direction: row;
		text-decoration: none;
		justify-self: center;
		align-items: center;
		margin-left: .5rem;
	}

	.logo{
		margin-left: 1rem;
		width: 3.5rem;
		height: 3.5rem;
	}

	.logoText{
		font-family: "switzer";
		font-style: italic;
		font-weight: 400;
		color: #1e1e1e;
		font-size: 1.4rem;
	}

	.nav-left {
		display: flex;
		align-items: center;
	}

	.nav-right{
		display: flex;
		justify-content: center;
		align-items: space-between;
		gap: 1.5rem;
		margin-right: 2.5rem;
	}

	.platforms {
		filter: grayscale(100%);
		opacity: .6;
		cursor: pointer;
		transition: .1s all;
		width: 1.6rem;
	}

	.windows{
		width: 1.8rem;
	}

	.platforms:hover{
		opacity: .8;
	}

	.platforms.active {
		filter: none;
		opacity: 1;
	}

</style>
