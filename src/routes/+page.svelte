<script>
    let { data } = $props();

    const member = data.members[0];
    import texture from '$lib/assets/texture.svg';
</script>

<!-- <h1>{member.name}</h1> -->
 
<main>
    <section class="hero">
        <h2>St<i>u</i>dio</h2>
        <h1>TIESBEEFTINK</h1>
        <picture>
            <img src={texture} alt="">
        </picture>
    </section>

    <article class="work">
        <picture>
            <img src="" alt="">
        </picture>
        <h2>Werk</h2>
        <p>Ik werk 2 tot 3 dagen in de week als chef in een restaurant. Het is een Franse keuken met hier en daar wat andere invloeden.</p>
    </article>

    <article class="hobby">
        <picture>
            <img src="" alt="">
        </picture>
        <h2>Hobby's</h2>
        <p>Ik ben naast school veel met muziek bezig. Ik produceer met 2 andere vrienden muziek voor artiesten in een studio. Voor nu is het vooral nog hobbymatig, maar het zou leuk zijn als ik hier later ook iets mee kan doen.</p>
    </article>

    <!-- <section>
        <h2>St<i>u</i>dio</h2>
        <h1>TIESBEEFTINK</h1>
        <picture>
            <img src={texture} alt="">
        </picture>
    </section> -->
</main>

<style>
    .hero {
        position: relative;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;

        h2,
        picture {
            position: absolute;
        }

        h2 {
            font-family: Calvino;
            font-size: 10rem;
            top: 9rem;
        }

        h1 {
            font-size: 8rem;
            font-weight: 400;
            top: 17.5rem;
            z-index: 100;
            position: fixed;
        }

        picture {
            top: 15rem;
        }
    }

    main {
        height: 400vh;
    }
    

    @supports (animation-timeline: scroll()) {
    body, .hero h2 {
        animation: first linear both;
        animation-timeline: scroll(block nearest);
    }
 
        @keyframes first {
            30% {
                transform: translateY(10rem);
            }
        }
    }

    @supports (animation-timeline: scroll()) {
    body, .hero img {
        animation: second linear both;
        animation-timeline: scroll(block nearest);
    }
 
        @keyframes second {
            30% {
                transform: translateY(-20rem);
            }
        }
    }

    @supports (animation-timeline: scroll()) {
    body, .hero h1 {
        animation: third linear both;
        animation-timeline: scroll(block nearest);
    }
 
        @keyframes third {
            20% {
                transform: translateY(-17.5rem);
            }

            100% {
                                transform: translateY(-17.5rem);

            }
        }
    }
 
</style>