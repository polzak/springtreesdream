<script>
	import Nav from '../components/Nav.svelte';

	export let segment;
</script>

<style>

	.wrapper {
		display: flex;
		flex-direction: column;
		min-height: 100vh;
	}
	
	main {
		position: relative;
		max-width: 56em;
		background-color: white;
		padding: 2em;
		margin: 0 auto;
		box-sizing: border-box;
		flex-grow: 1;
	}

	nav {
		flex-shrink: 0;
	}

	footer {
		background-color: cornflowerblue;
		flex-shrink: 0;
		min-height: 70px;
		text-align: center;
	}

	footer p {
		color: white;
		font-size: 1.2rem;
	}

	footer p a {
		text-decoration: none;;
	}

</style>

<div class="wrapper">
	<nav>
		<Nav {segment}/>
	</nav>
	<main>
		<slot></slot>
	</main>
	<footer>
		<p><a href="http://www.podbbang.com/ch/11200">지상 최대의 영어 작전 팟캐스트</a></p>
		<p>봄나무가 꾸는 꿈 Spring Trees Dream</p>
	</footer>
</div>