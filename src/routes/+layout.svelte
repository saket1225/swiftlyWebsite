<script>
    import Header from './Header.svelte';    
    import { currentOs } from './store.js';
    import Hero from './Hero.svelte'
    import CmdMac from './CmdMac.svelte';
    import CmdWindows from './CmdWindows.svelte';
    import CmdLinux from './CmdLinux.svelte';
    import Frameworks from './Frameworks.svelte';
    import './styles.css';

    import { tabsLinuxHeaders, frameworkLinux } from './linuxTerminal.js'
    import { tabsWindowsHeaders, frameworkWindows } from './windowsTerminal.js'
    import { tabsMacHeaders, frameworkMac } from './macTerminal.js'
</script>

<div class="app">
    <Header />
    <Hero />
    
    {#if $currentOs === 'mac'}
        <CmdMac tabs={tabsMacHeaders}/>
    {:else if $currentOs === 'windows'}
        <CmdWindows tabs={tabsWindowsHeaders}/>
    {:else if $currentOs === 'linux'}
        <CmdLinux tabs={tabsLinuxHeaders}/> <!-- pass tabs here -->
    {/if}

    <div class="divider"></div>

    <Frameworks />
    {#if $currentOs === 'mac'}
        <CmdMac tabs={frameworkMac}/>
    {:else if $currentOs === 'windows'}
        <CmdWindows tabs={frameworkWindows}/>
    {:else if $currentOs === 'linux'}
        <CmdLinux tabs={frameworkLinux}/> <!-- pass tabs here -->
    {/if}
</div>

<style>
	body{
		background: #fff;
	}

    .divider{
        position: absolute;
        inset: 0;
        top: 100%;
        width: 100%;
        height: 3px;
        background: #B9B9BB;
    }
</style>
