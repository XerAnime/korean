<script>
	import '../app.css';
	import Header from './Components/Header.svelte';
	export let data;
	let headerData = {
		siteName: data.siteName,
		navLinks: [{ text: 'Cool site for dramas', url: 'https://dramacool.pa' }]
	};
</script>

<div class="container bg-sky-300 p-7">
	<Header {headerData} />
	<main>
		<slot />
	</main>
</div>
