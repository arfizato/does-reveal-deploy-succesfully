<script>
	// @ts-nocheck
/* ------------------------------- Components ------------------------------- */
	import { onMount } from 'svelte';

/* --------------------------------- plugins -------------------------------- */
	import Reveal from 'reveal.js';

	import Simplemenu from './revealjs-plugins/simplemenu/plugin/simplemenu/simplemenu.esm.js';
	import Verticator from './revealjs-plugins/verticator/plugin/verticator/verticator.esm.js';
	import Animate from './revealjs-plugins/animate/animate.esm.js';
/* ------------------------------- stylesheets ------------------------------ */
    import 'reveal.js/dist/reveal.css';
    import 'reveal.js/dist/theme/black.css';
    import 'reveal.js/plugin/highlight/monokai.css';
	import 'animate.css';

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
			plugins: [ Animate, Verticator, Simplemenu],//Markdown, Highlight, Notes,
			verticator: {
				csspath: './revealjs-plugins/verticator/plugin/verticator/verticator.css'
			},
			simplemenu: {
				csspath: false
			},
			
			animated: {
				H1: { animated: 'slideInDown' },
				IMG: { animated: 'backInDown', repeat: 'repeat-2', speed: 'slower' },
				P: { animated: 'bounceInRight', speed: 'fast' },
				UL: { animated: 'jello', repeat: 'infinite', speed: 'slower' }
			},
		});
	});
</script>

<div class="reveal">
	<div class="slides">
		<section id="0"><h1>1</h1></section>
		<section id="1"><ul>2</ul></section>
		<section id="2"><h1>3</h1></section>
		<section id="3">
            <section><p>4.1</p></section>
            <section><p>4.2</p></section>
            <section><p>4.3</p></section>
            <section><p>4.4</p></section>

        </section>
        <section id="4"><ul>5</ul></section>

	</div>
</div>


<style>
    .reveal {
        width: calc(100vw - 200px);
        height: 100%;
    }
</style>