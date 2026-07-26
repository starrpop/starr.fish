<script lang="ts">
	import { resolve } from '$app/paths';
	import { page } from '$app/state';
	import starrHeader from '$lib/images/starr-header.png';
	import menuIcon from '$lib/images/menu-icon.png';
	import editorial from '$lib/images/editorial.png';
	import editorialActive from '$lib/images/editorial-active.png';
	import animatic from '$lib/images/animatic.png';
	import illustration from '$lib/images/illustration.png';
	import about from '$lib/images/about.png';
	import aboutActive from '$lib/images/about-active.png';
</script>

<header>
	<section>
		<span class="starr-header">
			<picture>
				<img src={starrHeader} alt="Starr Bialk Header" />
			</picture>
		</span>
		<span class="menu-icon">
			<picture>
				<img src={menuIcon} alt="Menu Icon" />
			</picture>
		</span>
	</section>
	<nav>
		<ul>
			<li aria-current={page.url.pathname === '/' ? 'page' : undefined}>
				<a href={resolve('/')}>
					<img src={page.url.pathname === '/' ? editorialActive : editorial} alt="Editorial Link" />
				</a>
			</li>
			<li aria-current={page.url.pathname === '/animatic' ? 'page' : undefined}>
				<a href={resolve('/animatic')}>
					<img src={animatic} alt="Animatic Link" />
				</a>
			</li>
			<li aria-current={page.url.pathname === '/illustration' ? 'page' : undefined}>
				<a href={resolve('/illustration')}>
					<img src={illustration} alt="Illustration Link" />
				</a>
			</li>
			<li aria-current={page.url.pathname === '/about' ? 'page' : undefined}>
				<a href={resolve('/about')}>
					<img src={page.url.pathname === '/about' ? aboutActive : about} alt="About Link" />
				</a>
			</li>
		</ul>
	</nav>
</header>

<style>
	header {
		display: flex;
		flex-direction: column;
		align-items: center;
		margin-top: 3rem;
	}

	section {
		display: flex;
		flex-direction: row;
		gap: 3rem;
	}

	.menu-icon {
		display: flex;
		flex-direction: column;
	}

	ul {
		display: flex;
		gap: 3rem;
		margin-top: 3rem;
		list-style: none;
	}
</style>
