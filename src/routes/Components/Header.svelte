<script>
	export let headerData;
	import { Search } from 'lucide-svelte';
</script>

<header>
	<div class="container flex justify-between font-serif px-4 text-3xl">
		<h1>{headerData.siteName}</h1>
		<nav>
			<ul>
				{#each headerData.navLinks as link}
					<li>
						<a href={link.url}
							><span class="text-white italic md:tracking-[.30em]">{link.text}</span>
						</a>
					</li>
				{/each}
			</ul>
		</nav>

		<form>
			<div class="relative flex flex-col items-end">
				<input class="px-4 py-1 text-base" type="text" id="search" placeholder="Search" />

				<button class="absolute bg-orange-300 p-1">
					<Search />
				</button>
			</div>
		</form>
	</div>
</header>
