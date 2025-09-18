<script>
	import '$lib/css/app.css';
	import favicon from '$lib/assets/favicon.svg';
    import texture from '$lib/assets/texture.svg';


	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>

<main>
	<section class="hero">
        <h2 class="subtitle">St<i>u</i>dio</h2>
        <h1 class="title">TIESBEEFTINK</h1>
        <picture class="image">
            <img src={texture} alt="">
        </picture>
    </section>
	
	{@render children?.()}
</main>

<style>
	    :root {
        font-size: clamp(1.25rem, 3vw, 2.5rem);
    }

    @keyframes scrollTitle {
        100% {
            top: 0;
        }
    }

    @keyframes scrollSubtitle {
        100% {
            translate: 0 5rem;
        }
    }

    @keyframes scrollImage {
        100% {
            translate: 0 -10rem;
        }
    }

    .hero {
        display: flex;
        justify-content: center;
        align-items: center;
        height: 100vh;
    
    .subtitle {
        position: absolute;
        top: calc(50vh - 7.5rem);
        font-size: 3rem;
        font-family: Calvino;
        
        @supports (animation-timeline: scroll()) {
            & {
                animation: scrollSubtitle linear both;
                animation-timeline: scroll(root y);
                animation-range: 0 75vh;
            }
        }
    }
    
    .title {
        position: fixed;
        top: calc(50vh - 4rem);
        font-size: 2rem;
        z-index: 2;
        font-weight: 400;
        
        @supports (animation-timeline: scroll()) {
            & {
                animation: scrollTitle linear both;
                animation-timeline: scroll(root y);
                animation-range: 0 75vh;
            }
        }
    }
    
    .image {
        width: 7rem;
        aspect-ratio: 2 / 3;

        z-index: 1;
        
        img {
            /* object-fit: cover; */
            width: 100%;
            height: 100%;
        }
        
        @supports (animation-timeline: scroll()) {
            & {
                animation: scrollImage linear both;
                animation-timeline: scroll(root y);
                animation-range: 0 75vh;
            }
        }
    }
    }
</style>