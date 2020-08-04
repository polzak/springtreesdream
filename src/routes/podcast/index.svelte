<script context="module">
	export function preload({ params, query }) {
		return this.fetch(`https://swapi.dev/api/people/`).then(r => r.json()).then(people => {
			return { people: people.results };//The preload function should return 
							//an object whose property names are the names of props 
							//accepted by the page component and 
							//whose property values will become the prop values
							//https://swapi.dev/api/people/1
							//blog.json
		});
	}
</script>

<script>
	export let people;
</script>

<style>
	ul {
		margin: 0 0 1em 0;
		line-height: 1.5;
	}
</style>

<svelte:head>
	<title>Blog</title>
</svelte:head>

<h1>Recent posts</h1>

<ul>
	{#each people as p, i}
		<!-- we're using the non-standard `rel=prefetch` attribute to
				tell Sapper to load the data for the page as soon as
				the user hovers over the link or taps it, instead of
				waiting for the 'click' event -->
		<li><a rel='prefetch' href='podcast/{i+1}'>{p.name}</a></li>
	{/each}
</ul>