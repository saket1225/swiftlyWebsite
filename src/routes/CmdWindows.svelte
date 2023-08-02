<script>
    import min from '$lib/images/minWin.svg';
    import max from '$lib/images/maxWin.svg';
    import close from '$lib/images/closeWin.svg';

    let activeTab = 'init'; // Default active tab

    function switchTab(tab) {
        activeTab = tab;
    }
</script>

<div class="cmdWindows">
	<div class="navWindows">
        <div class="emptyArea"></div>
        <div class="tabs">
            <div class="tab" class:active={activeTab === 'init'} on:click={() => switchTab('init')}>init</div>
            <div class="tab" class:active={activeTab === 'start'} on:click={() => switchTab('start')}>start</div>
            <div class="tab" class:active={activeTab === 'makeapp'} on:click={() => switchTab('makeapp')}>makeapp</div>
            <div class="tab" class:active={activeTab === 'install'} on:click={() => switchTab('install')}>install</div>
            <div class="tab" class:active={activeTab === 'run'} on:click={() => switchTab('run')}>run</div>
        </div>
        <div class="emptyAreaBetween"></div>
        <div class="controls">
            <div class="control">
                <img src={min} alt="minimize icon">
            </div>
            <div class="control">
                <img src={max} alt="maximize icon">
            </div>
            <div class="control">
                <img src={close} alt="close icon">
            </div>
        </div>
    </div>

    <div class="content">
        {#if activeTab === 'init'}
            <h2>
                shubhastro@MBP no-curlybraces % <span class="highlight">source swiftly init &ltgit-repo@url || name&gt <br></span>
                <span class="green">✓</span> Checked swiftly <br>
                <span class="green">✓</span> Git repository cloned <br>
                <span class="green">✓</span> Project 'lean' ready <br>
                <span class="green">✓</span> Requirements installed <br>
                <span class="green">✓</span> All checks completed swiftly <br>
                ✨ Project 'lean' initiated successfully :) <br>
                <span class="emphasize">(venvlean) shubhastro@MBP lean %</span>
            </h2>
        {:else if activeTab === 'start'}
            <h2>
                shubhastro@MBP no-curlybraces % <span class="highlight">source swiftly start<br></span>
                <span class="green">✓</span> Checked swiftly <br>
                <span class="green">✓</span> Git repository cloned <br>
                <span class="green">✓</span> Project 'lean' ready <br>
                <span class="green">✓</span> Requirements installed <br>
                <span class="green">✓</span> All checks completed swiftly <br>
                ✨ Project 'lean' initiated successfully :) <br>
                <span class="emphasize">(venvlean) shubhastro@MBP lean %</span>
            </h2>
        {:else if activeTab === 'makeapp'}
            <h2>
                shubhastro@MBP no-curlybraces % <span class="highlight">source swiftly makeapp <br></span>
                <span class="green">✓</span> Checked swiftly <br>
                <span class="green">✓</span> Git repository cloned <br>
                <span class="green">✓</span> Project 'lean' ready <br>
                <span class="green">✓</span> Requirements installed <br>
                <span class="green">✓</span> All checks completed swiftly <br>
                ✨ Project 'lean' initiated successfully :) <br>
                <span class="emphasize">(venvlean) shubhastro@MBP lean %</span>
            </h2>
        {:else if activeTab === 'install'}
            <h2>
                shubhastro@MBP no-curlybraces % <span class="highlight">source swiftly install &lspackage name&gt <br></span>
                <span class="green">✓</span> Checked swiftly <br>
                <span class="green">✓</span> Git repository cloned <br>
                <span class="green">✓</span> Project 'lean' ready <br>
                <span class="green">✓</span> Requirements installed <br>
                <span class="green">✓</span> All checks completed swiftly <br>
                ✨ Project 'lean' initiated successfully :) <br>
                <span class="emphasize">(venvlean) shubhastro@MBP lean %</span>
            </h2>
        {:else if activeTab === 'run'}
            <h2>
                shubhastro@MBP no-curlybraces % <span class="highlight">swiftly run <br></span>
                <span class="green">✓</span> Checked swiftly <br>
                <span class="green">✓</span> Git repository cloned <br>
                <span class="green">✓</span> Project 'lean' ready <br>
                <span class="green">✓</span> Requirements installed <br>
                <span class="green">✓</span> All checks completed swiftly <br>
                ✨ Project 'lean' initiated successfully :) <br>
                <span class="emphasize">(venvlean) shubhastro@MBP lean %</span>
            </h2>
        {/if}
    </div>

    <div class="footer">
        <h2>One command. Ready. Set. Go!</h2>
        <a href="https://youtube.com/" target="_blank">Read Documentation</a>
    </div>
</div>
<style>	
    @import url('https://fonts.googleapis.com/css2?family=Source+Code+Pro:wght@200;300;400;500;600;700;800;900&family=Source+Sans+3:wght@200;300;400;500;600;700;800;900&display=swap');
    @import url('https://fonts.googleapis.com/css2?family=Source+Sans+3:wght@200;300;400;500;600;700;800;900&display=swap');

    .cmdWindows{
        position: relative;
        transform: translateX(-50%);
        margin-top: 3rem;
        border-radius: 10px;
        left: 50%;
        display: flex;
        flex-direction: column;
        background: #FFFFFF;
        box-shadow: 0px 0px 50px 0px rgba(0, 0, 0, 0.15);
        width: 42rem;
    }

    .navWindows{
        display: flex;
    }

    .controls{
        display: flex;
        align-items: center;
        gap: 0.4rem;
        padding: 0 1rem;
        border-bottom: 1px solid #B9B9BB;
    }

    .controls .control{
        position: relative;
        top: .2rem;
        transform: scale(1.1);
    }

    .controls .red{
        background: #ED6A5F;
    }
    
    .controls .yellow{
        background: #F5BF4F;
    }
    
    .controls .green{
        background: #61C554;
    }

    .tabs{
        display: flex;
    }

    .tabs .tab{
        padding: 8px 15px;
        border-right: 0.5px solid #B9B9BB;
        font-family: 'Switzer';
        color: #5B5B5C;
        font-weight: 300;
        cursor: pointer;
        transition: .2s all;
        border-bottom: 1px solid #B9B9BB;
    }

    .tabs .tab:hover{
        background: #fbf9f9;
    }
    
    .tabs .active:hover{
        background: #fff;
    }

    .tabs .active{
        color: #000;
        font-weight: 400;
        border-bottom: 1px solid #fff;
    }

    .emptyArea{
        width: 7rem;
        border-bottom: 1px solid #B9B9BB;
        border-right: 1px solid #B9B9BB;
    }

    .emptyAreaBetween{
        width: 100%;
        border-bottom: 1px solid #B9B9BB;
    }

    .content h2{
        font-family: 'Source Code Pro';
        font-size: 14px;
        padding: 5px 15px;
        font-weight: 400;
        color: #5B5B5C;
    }

    .content h2 .highlight{
        background: linear-gradient(97deg, #C0F2FF 0%, #E3FEE7 100%);
        color: #000;
        font-weight: 500;
        padding: 0.3rem 0.5rem;
    }

    .content h2 .emphasize{
        color: #000;
        font-weight: 500;
    }
    
    .content h2 .green{
        color: #57BF38;
    }

    .footer{
        display: flex;
        margin-top: 3rem;
        justify-content: space-between;
        align-items: center;
        padding: 0 1rem;
        background: #FAFAFA;
        border-top: 0.5px solid #B9B9BB;
        font-family: 'Source Sans 3';
    }

    .footer h2{
        font-size: 16px;
        font-weight: 400;
        color: #686869;
    }
    
    .footer a{
        text-decoration: none;
        color: #2F80ED;
        transition: 0.1s all;
    }
    
    .footer a:hover{
        opacity: 0.7;
    }
</style>
