<script context="module">
	export async function preload({ params, query }) {
		// the `slug` parameter is available because this file is called [slug].svelte
		// console.log(params);
		// console.log(query);
		const res = await this.fetch(`https://swapi.dev/api/people/${params.slug}`);
									//https://swapi.dev/api/people/1 
		const data = await res.json();

		if (res.status === 200) {
			return { person: data };
		} else {
			this.error(res.status, data.message);
		}
	}
</script>

<script>
	export let person;
</script>

<svelte:head>
	<title>{person.name}</title>
</svelte:head>

<h1>{person.name}</h1>
<p>{person.gender}</p>
<p>{person.height}</p>

<!-- <div class='content'>
	{@html post.html}
</div> -->
