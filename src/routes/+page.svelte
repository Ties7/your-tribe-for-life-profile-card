<script>
    let { data } = $props();

    const member = data.members[0];
    import texture from '$lib/assets/texture.svg';
</script>

<!-- <h1>{member.name}</h1> -->
<div class="content-wrapper">
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

    <article class="content hobby">
        <picture>
            <img src="" alt="">
        </picture>
        <h2>Hobby's</h2>
        <p>Ik ben naast school veel met muziek bezig. Ik produceer met 2 andere vrienden muziek voor artiesten in een studio. Voor nu is het vooral nog hobbymatig, maar het zou leuk zijn als ik hier later ook iets mee kan doen.</p>
    </article>
</div>

<style>
    .content-wrapper {
        display: flex;
        justify-content: center;
        height: 200vh;
    }
    
    .content {
        width: 10rem;

        h2, p {
            font-size: .7rem;
        }
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