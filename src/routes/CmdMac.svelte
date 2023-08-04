<script>
    let activeTab = 'init'; // Default active tab

    function switchTab(tab) {
        activeTab = tab;
    }
</script>

<div class="cmdMac">
	<div class="navMac">
        <div class="controls">
            <div class="control red"></div>
            <div class="control yellow"></div>
            <div class="control green"></div>
        </div>
        <div class="tabs">
            <div class="tab" class:active={activeTab === 'init'} on:click={() => switchTab('init')}>init</div>
            <div class="tab" class:active={activeTab === 'start'} on:click={() => switchTab('start')}>start</div>
            <div class="tab" class:active={activeTab === 'makeapp'} on:click={() => switchTab('makeapp')}>makeapp</div>
            <div class="tab" class:active={activeTab === 'install'} on:click={() => switchTab('install')}>install</div>
            <div class="tab" class:active={activeTab === 'run'} on:click={() => switchTab('run')}>run</div>
        </div>
        <div class="emptyArea"></div>
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

    .cmdMac{
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

    .navMac{
        display: flex;
    }

    .controls{
        display: flex;
        align-items: center;
        gap: 0.4rem;
        padding: 0 1rem;
        border-right: 0.5px solid #B9B9BB;
        border-bottom: 1px solid #B9B9BB;
    }

    .controls .control{
        width: 0.8rem;
        height: 0.8rem;
        border-radius: 50%;
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
        font-weight: 500;
        border-bottom: 1px solid #fff;
    }

    .emptyArea{
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

    @media only screen and (max-width: 1200px){
    .cmdMac{
        width: 80%;
    }
}

@media only screen and (max-width: 992px){
    .cmdMac{
        width: 90%;
    }
    .content h2{
        font-size: 12px;
    }
    .footer h2, a{
        font-size: 0.8rem;
    }
}

@media only screen and (max-width: 768px){
    .cmdMac{
        width: 90%;
    }
    .tab{
        padding: 8px 10px !important;
        font-size: 0.9rem; /* Increase font size */
    }
    .content h2{
        font-size: 12px; /* Increase font size */
    }
    .footer h2, a{
        font-size: 0.9rem; /* Increase font size */
    }
}

    @media only screen and (max-width: 576px){
        .cmdMac{
            width: 90%;
        }
        .emptyArea{
            width: 3rem;
        }

        .emptyAreaBetween{
            width: 0rem;
        }

        .content h2 .highlight{
            padding: 3px;
            display: inline-block;
            width: 100%;
        }

        .tabs{
            width: 100%;
            display: flex;
            overflow-x: auto; /* Enable horizontal scrolling */
            scrollbar-width: none; /* Hide scrollbar for Firefox */
            -ms-overflow-style: none; /* Hide scrollbar for IE and Edge */
            flex-grow: 1; /* Allow the tabs to take up the remaining space */
        }

        .tabs::-webkit-scrollbar {
            display: none; /* Hide scrollbar for Chrome, Safari and Opera */
        }

        .tab{
            flex: 0 0 auto; /* Prevent flex items from shrinking */
            /* Increase the width of the tab as needed */
        }

        .controls{
            position: sticky;
            right: 0; /* Stick to the right */
        }

        .content h2{
            font-size: 12px; /* Further increase font size */
        }

        .footer{
            flex-direction: column;
            padding-bottom: 1rem;
        }

        .footer h2, a{
            font-size: 1rem; /* Further increase font size */
        }
    }
</style>
