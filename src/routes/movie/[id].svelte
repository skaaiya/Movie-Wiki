<script context="module">
  export async function load({fetch, params}){
    const res = await fetch(`https://api.themoviedb.org/3/movie/${params.id}?api_key=2e88b624c056d3a65bab6ee674dc1b1f&language=en-US`)
    const movieDetail = await res.json();
    if(res.ok){
      return{
        props: { movieDetail }
      };
    }
  }
</script>

<script>
  export let movieDetail;
</script>

<div class="details">
  <div class="img-container">
    <img src={'https://image.tmdb.org/t/p/original' + movieDetail.backdrop_path} alt={movieDetail.title}>
  </div>
  <div class="txt-container">
    <h1>{movieDetail.title}</h1>
  </div>
</div>