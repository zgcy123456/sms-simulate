<script context="module">
    export async function load({ fetch }){
        const res = await fetch(`http://localhost:8080/todolist`);
        // const res = await fetch(`https://api.themoviedb.org/3/movie/changes?page=1`);
        // res.headers.
        const data = await res.json();
        console.log(66666);
        console.log(data);
        if(res.ok){
            return{
                props:{popular: data.result}
            }
        }
    }
    

</script>

<script>
    import PopularMovies from "./components/PopularMovies.svelte";
    export let popular;
    console.log(popular);
</script>



<h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>
<p>visit echarts <a href="/worldmap">world map</a> </p>

<section>
    <PopularMovies {popular}/>
</section>