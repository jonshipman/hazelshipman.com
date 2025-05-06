<script lang="ts">
	import { page } from '$app/stores';

	let DESTINATION = 'https://www.redbubble.com/people/jonshipman/shop?artistUserName=jonshipman&asc=u&collections=4245161';

	$: url = $page.url.toString();
</script>

<svelte:head>
	<title>HazelShipman.com</title>
	<meta property="og:url" content={url} />
	<meta property="og:type" content="website" />
	<meta property="og:title" content="Hazel Shipman" />
	<meta property="og:description" content="" />
	<meta property="og:image" content="{url}favicon.png" />

	<meta http-equiv="refresh" content="1; url={DESTINATION}" />
</svelte:head>
