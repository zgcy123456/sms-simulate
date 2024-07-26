<script>
    export let popular;
    console.log(popular);
</script>

<h1>popular movies</h1>
<div class="popular-movies">
    {#each popular as movie}
        <h1>{movie.title}</h1>        
    {/each}
</div>