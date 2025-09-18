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

 
</style>