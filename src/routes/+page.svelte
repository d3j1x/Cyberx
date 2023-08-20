<script>
    import { Alert } from 'flowbite-svelte';
	import { Blockquote } from 'flowbite-svelte';
  	import { Icon } from 'flowbite-svelte-icons';
	import Terminal from '$lib/components/Terminal.svelte';
</script>

<svelte:head>
	<title>Cyber X</title>
	<meta name="description" content="Cyber Security | Secrets - Resources - Hints - Tips ..." />
</svelte:head>


<div class="flex justify-center items-center p-8">
	<Blockquote alignment="center" size="xl" >
		<Icon name="quote-solid" class="w-10 h-10 text-gray-400 dark:text-gray-600" />
		<span>"Cyber X Is Just Awesome Opensource.
			<br>Best Of Cybersecurity Tips Hint Source..."</span>
	</Blockquote>
</div>


<div class="flex mt-3 justify-center items-center">
	<!-- <h1 class="text-3xl font-semibold">Welcome to CyberX.</h1> -->
	<Terminal />
</div>



<div class="text-center p-8">
	<Alert>
		<span>CyberX alert!</span> We Develope.
	</Alert>
</div>

<!-- <p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p> -->
