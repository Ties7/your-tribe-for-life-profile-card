<script>
    let { data } = $props();

    const member = data.members[0];
    import texture from '$lib/assets/texture.svg';
</script>

<!-- <h1>{member.name}</h1> -->
 
<main>
    <section class="hero">
        <h2 class="subtitle">St<i>u</i>dio</h2>
        <h1 class="title">TIESBEEFTINK</h1>
        <picture class="image"><img src={texture} alt=""></picture>
    </section>

    <article class="content work">
        <picture>
            <img src="" alt="">
        </picture>
        <h2>Werk</h2>
        <p>Ik werk 2 tot 3 dagen in de week als chef in een restaurant. Het is een Franse keuken met hier en daar wat andere invloeden.</p>
    </article>

    <article class="content hobby">
        <picture>
            <img src="" alt="">
        </picture>
        <h2>Hobby's</h2>
        <p>Ik ben naast school veel met muziek bezig. Ik produceer met 2 andere vrienden muziek voor artiesten in een studio. Voor nu is het vooral nog hobbymatig, maar het zou leuk zijn als ik hier later ook iets mee kan doen.</p>
    </article>
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

    .content {
        width: 10rem;
    }

    .work {
        top: 140vh;
        position: absolute;
    }

    .hobby {
        top: 190vh;
        position: absolute;
    }
 
</style>