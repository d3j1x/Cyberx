<script>
    import { Alert } from 'flowbite-svelte';
	import Terminal from '$lib/components/Terminal.svelte';
</script>

<svelte:head>
	<title>Cyber X</title>
	<meta name="description" content="Cyber Security | Secrets - Resources - Hints - Tips ..." />
</svelte:head>

<div class="flex mt-16 justify-center items-center">
	<!-- <h1 class="text-3xl font-semibold">Welcome to CyberX.</h1> -->
	<Terminal />
</div>



<div class="text-center p-8">
	<Alert>
		<span>CyberX alert!</span> We Develope.
	</Alert>
</div>

<!-- <p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p> -->
