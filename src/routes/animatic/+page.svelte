<script lang="ts">
	import videoStub from '$lib/images/video-stub.png';
</script>

<svelte:head>
	<title>Animatic</title>
	<meta name="description" content="Starr B. animatic web portfolio" />
</svelte:head>

<section>
	<img src={videoStub} alt="Video Stub" />
	<img src={videoStub} alt="Video Stub" />
	<img src={videoStub} alt="Video Stub" />
</section>

<style>
	section {
		display: flex;
		flex-direction: column;
		gap: 6rem;
		margin-top: 3rem;
	}
</style>
