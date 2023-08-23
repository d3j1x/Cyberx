<script>
    import { Alert } from 'flowbite-svelte';
	import { Blockquote } from 'flowbite-svelte';
  	import { Icon } from 'flowbite-svelte-icons';
	import Terminal from '$lib/components/Terminal.svelte';
	import { Card, Button } from 'flowbite-svelte';
	import pathseek from '$lib/img/pathway.png';
  	
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

<div class="flex my-10 justify-center items-center">
	<Card img={pathseek} reverse={true} class="mb-4">
	  <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">CYBERSECURITY CAREER PATHWAY
	</h5>
	  <p class="mb-3 font-normal text-gray-700 dark:text-gray-400 leading-tight">There are many opportunities for workers to start and advance their careers within cybersecurity...</p>
	  <a href="https://www.cyberseek.org/pathway.html" target="_blank" rel="noreferrer">
		<Button>
		Explore <Icon name="arrow-right-outline" class="w-3.5 h-3.5 ml-2 text-white" />
	  </Button>
	  </a>
	</Card>
	
</div>



<div class="text-center p-8">
	<Alert>
		<span>CyberX alert!</span> We Develope.
	</Alert>
</div>

<!-- <p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p> -->
