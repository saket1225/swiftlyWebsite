<script>
    export let tabs = []; // here we define the tabs as a prop

    let activeTab; // Default active tab

    // Reactive statement to update activeTab when tabs changes
    $: if (tabs.length > 0) {
        activeTab = tabs[0].label;
    }

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
            {#each tabs as tab}
                <div class="tab" class:active={activeTab === tab.label} on:click={() => switchTab(tab.label)}>{tab.label}</div>
            {/each}
        </div>
        <div class="emptyArea"></div>
    </div>

    <div class="content">
        {#each tabs as tab (tab.label)}
            {#if activeTab === tab.label}
                <h2>
                    {@html tab.content}
                </h2>
            {/if}
        {/each}
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
        white-space: nowrap;
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

        /* content styling in style.css */

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

        .footer{
            flex-direction: column;
            padding-bottom: 1rem;
        }

        .footer h2, a{
            font-size: 1rem; /* Further increase font size */
        }
    }
</style>
