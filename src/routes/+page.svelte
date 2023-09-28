<script>
	import * as config from '$lib/config';
	export let data;
</script>

<svelete:head>
	<title>{config.title}</title>
</svelete:head>

<section>
	<ul class="posts">
		{#each data.posts as post}
			<li class="post">
				<a href={post.slug} class="title">{post.title}</a>
				<p class="date">{post.date}</p>
				<p class="description">{post.description}</p>
			</li>
		{/each}
	</ul>
</section>
