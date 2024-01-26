<script lang="ts">
	import { dev } from '$app/environment';
	import { page } from '$app/stores';

	const DESTINATION =
		'https://www.amazon.com/hz/wishlist/ls/3PBM618DVH2V5?ref_=list_d_wl_lfu_nav_7';

	$: url = $page.url.toString();
</script>

<svelte:head>
	<title>HazelShipman.com</title>
	<meta property="og:url" content={url} />
	<meta property="og:type" content="website" />
	<meta property="og:title" content="Hazel Shipman" />
	<meta property="og:description" content="" />
	<meta property="og:image" content="{url}favicon.png" />

	{#if !dev}
		<meta http-equiv="refresh" content="1; url={DESTINATION}" />
	{/if}
</svelte:head>
