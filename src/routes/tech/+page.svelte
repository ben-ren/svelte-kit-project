<svelte:head>
    <title>Technologies</title>
    <meta name="description" content="Page about a variety of interesting technologies"/>
</svelte:head>

<div class="text-column">
    
    <h1>Tech</h1>
    <nav>
        <ul>
            <li>
                <a href="/tech/robotics">Robotics</a>
            </li>
            <li>
                <a href="/tech/chemistry">Chemistry</a>
            </li>
        </ul>
    </nav>
    <p>Welcome to the tech corner. Here we'll tell you about a variety of interesting technologies.</p>
    <p>Click one of the links to see information about a technology category.</p>
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
</style>