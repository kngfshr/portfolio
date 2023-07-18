<script lang="ts">
	import { onMount } from 'svelte';

    export let id = "";
	export let once = false;
	export let top = 0;
	export let bottom = 0;
	export let left = 0;
	export let right = 0;

	let intersecting = false;
	let container: Element;

	onMount(() => {
		if (typeof IntersectionObserver !== 'undefined') {
			const rootMargin = `${bottom}px ${left}px ${top}px ${right}px`;

			const observer = new IntersectionObserver(entries => {
				intersecting = entries[0].isIntersecting;
				if (intersecting && once) {
					observer.unobserve(container);
				}
			}, {
				rootMargin
			});

			observer.observe(container);
			return () => observer.unobserve(container);
		}

		function handler() {
			const bcr = container.getBoundingClientRect();
			intersecting = (
				(bcr.bottom + bottom) > 0 &&
				(bcr.right + right) > 0 &&
				(bcr.top - top) < window.innerHeight &&
				(bcr.left - left) < window.innerWidth
			);

			if (intersecting && once) {
				window.removeEventListener('scroll', handler);
			}
		}

		window.addEventListener('scroll', handler);
		return () => window.removeEventListener('scroll', handler);
	});
</script>

<style lang="postcss">
	section {
        @apply py-16 sm:py-20 lg:py-24 text-center mx-auto;
		display: grid;
		place-items: center;
		align-content: center;
		min-height: 100vh;
	}
    .hidden {
		opacity: 0;
        filter: blur(3px);
        transform: translateX(-100%);
		transition: all 0.5s;
	}

	.show {
		opacity: 1;
        transform: translateX(0);
        transition: all 0.5s;
	}
</style>

<section id={id} bind:this={container} class:hidden={!intersecting} class:show={intersecting}>
	<slot></slot>
</section>