<script lang="ts">
	import { Button } from '$lib/components/ui/button/index.js';
	import Input from '$lib/components/ui/input/input.svelte';
	const corrPass = ['vaionetta', 'titita', 'bonini', 'onyelkis'];

	let input = $state('');
</script>

<main class="flex flex-col gap-y-5">
	<h1 class="text-3xl font-bold text-violet-500">Hiiiiiiiiiiiiiiiiiiiiiiiii</h1>

	<p class="text-2xl text-violet-500">
		Esta pagina esta dedicada para mi mochito, si eres ella ingresa su apodo aqui abajo:
	</p>
	<Input type="text" id="pass" bind:value={input} class="w-52" />

	{#if corrPass.includes(input.toLowerCase())}
		<p aria-label="Link to next page" class="text-2xl text-violet-500">
			MI amorcito bello, ERES TUUUUUUUUUUUUUUUUUUUUUUUU, ve a la siguiente pagina dandole click al
			boton ->
		</p>
		<a href="/valid" class="hover:cursor-pointer">
			<Button aria-label="Button to next page" class="bg-violet-400">Siguiente pagina</Button>
		</a>
	{/if}
</main>
