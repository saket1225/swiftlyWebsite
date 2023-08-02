<script>
	import Header from './Header.svelte';	
	import { currentOs } from './store.js';
	import Hero from './Hero.svelte'
	import CmdMac from './CmdMac.svelte';
	import CmdWindows from './CmdWindows.svelte';
	import CmdLinux from './CmdLinux.svelte';
	import './styles.css';
</script>

<div class="app">
	<Header />
	<Hero />
	
	{#if $currentOs === 'mac'}
    <CmdMac />
	{:else if $currentOs === 'windows'}
		<CmdWindows />
	{:else if $currentOs === 'linux'}
		<CmdLinux />
	{/if}
</div>

<style>
	body{
		background: #fff;
	}
</style>
