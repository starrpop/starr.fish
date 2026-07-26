<script lang="ts">
	import hello from '$lib/images/hello.png';
</script>

<svelte:head>
	<title>About</title>
	<meta name="description" content="About Starr B." />
</svelte:head>

<section>
	<img src={hello} alt="Hello" />
</section>

<style>
	section {
		display: flex;
		flex-direction: column;
		margin-top: 3rem;
	}
</style>
