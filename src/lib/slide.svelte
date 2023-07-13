<script>
	// @ts-nocheck
/* ------------------------------- Components ------------------------------- */
	import { onMount } from 'svelte';

/* --------------------------------- plugins -------------------------------- */
	import Reveal from 'reveal.js';

	import Simplemenu from './revealjs-plugins/simplemenu/plugin/simplemenu/simplemenu.esm.js';
	import Verticator from './revealjs-plugins/verticator/plugin/verticator/verticator.esm.js';
/* ------------------------------- stylesheets ------------------------------ */
    import 'reveal.js/dist/reveal.css';
    import 'reveal.js/dist/theme/black.css';
    import 'reveal.js/plugin/highlight/monokai.css';

	import './revealjs-plugins/verticator/plugin/verticator/verticator.css';
	import './revealjs-plugins/simplemenu/plugin/simplemenu/simplemenu.css';
/* -------------------------------- functions ------------------------------- */

/* ---------------------------- Liyfecycle Events --------------------------- */
	onMount(() => {
		// @ts-ignore
		const deck = new Reveal({
			autoAnimateEasing: 'ease',
			autoAnimateDuration: 1,
			hash: true,
			controls: true,
			progress: false
		});

		deck.initialize({
			plugins: [ Verticator, Simplemenu],//Markdown, Highlight, Notes, Animate,
			// animated: {
			// 	H1: { animated: 'slideInDown' },
			// 	IMG: { animated: 'backInDown', repeat: 'repeat-2', speed: 'slower' },
			// 	P: { animated: 'bounceInRight', speed: 'fast' },
			// 	UL: { animated: 'jello', repeat: 'infinite', speed: 'slower' }
			// },
			// verticator: {
			// 	csspath: 'reveal.js/plugin/verticator/plugin/verticator/verticator.css'
			// },
			// simplemenu: {
			// 	csspath: false
			// }
		});
	});
</script>

<div class="reveal">
	<div class="slides">
		<section id="0">1</section>
		<section id="1">2</section>
		<section id="2">3</section>
		<section id="3">
            <section>4.1</section>
            <section>4.2</section>
            <section>4.3</section>
            <section>4.4</section>

        </section>
        <section id="4">5</section>

	</div>
</div>


<style>
    .reveal {
        width: calc(100vw - 200px);
        height: 100%;
    }
</style>