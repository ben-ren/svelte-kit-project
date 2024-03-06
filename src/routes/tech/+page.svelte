<script>
    import AI from './artificial_intelligence/AI.svelte'
    import Chemistry from './chemistry/Chemistry.svelte'
    import Games from './games/Games.svelte'
    import Robotics from './robotics/Robotics.svelte'
    import Space from './space/Space.svelte'
    let linkNum = -1;

    function linkNumChange(val){
        linkNum = val
    }
</script>

<svelte:head>
    <title>Technologies</title>
    <meta name="description" content="Page about a variety of interesting technologies"/>
</svelte:head>

<div>
    <h1>Technology</h1>
    <nav>
        <ul>
            <li>
                <button class="hyperlink-button" on:click={() => linkNumChange(0)}>Games</button>
            </li>
            <li>
                <button class="hyperlink-button" on:click={() => linkNumChange(1)}>AI</button>
            </li>
            <li>
                <button class="hyperlink-button" on:click={() => linkNumChange(2)}>Space</button>
            </li>
            <li>
                <button class="hyperlink-button" on:click={() => linkNumChange(3)}>Robotics</button>
            </li>
            <li>
                <button class="hyperlink-button" on:click={() => linkNumChange(4)}>Chemistry</button>
            </li>
        </ul>
    </nav>
    
    <div>
        {#if linkNum < 0}
            <p>Welcome to the tech corner. Here we'll tell you about a variety of interesting technologies.</p>
            <p>Click one of the links to see information about a technology category.</p>
        {:else if linkNum == 0}
            <Games/>
        {:else if linkNum == 1}
            <AI/>
        {:else if linkNum == 2}
            <Space/>
        {:else if linkNum == 3}
            <Robotics/>
        {:else if linkNum == 4}
            <Chemistry/>
        {/if}
    </div>

    
</div>

<style>
    nav {
		display: flex;
		justify-content: center;
    }
    li {
		position: relative;
		height: 100%;
        margin-left: 10%;
	}
    ul{
        display: flex;
        margin-right: 5%;
        justify-content: center;
		align-items: center;
        list-style: none;
    }
    /* Style the button to resemble a hyperlink */
    .hyperlink-button {
        background: none;
        border: none;
        color: blue; /* Set the color to blue to resemble hyperlink */
        text-decoration: underline; /* Add underline to mimic hyperlink */
        cursor: pointer; /* Change cursor to pointer to indicate it's clickable */
        padding: 0;
        font: inherit;
    }
</style>