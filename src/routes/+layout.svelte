<script>
	import { i18n } from '$lib/i18n';
	import { ParaglideJS } from '@inlang/paraglide-sveltekit';
	import '../app.css'
	import Footer  from '../lib/components/Footer.svelte';

	/** @type {{children: import('svelte').Snippet}} */
	let { children } = $props();
</script>

<ParaglideJS {i18n}>
	<div class="app">
		

		<main>
			{@render children()}
		</main>
		<Footer/>
		
	</div>
</ParaglideJS>

<style>
	.app {
		display: flex;
		flex-direction: column;
		min-height: 100vh;
	}

	main {
		flex: 1;
		display: flex;
		flex-direction: column;
		padding: 1rem;
		width: 100%;
		max-width: 64rem;
		margin: 0 auto;
		box-sizing: border-box;
	}

	footer {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding: 12px;
	}

	footer a {
		font-weight: bold;
	}

	@media (min-width: 480px) {
		footer {
			padding: 12px 0;
		}
	}
</style>


