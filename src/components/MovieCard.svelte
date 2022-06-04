<script>
  export let movie;
</script>

<div class="movie-card">
  <div class="description">
    <h2>{movie.title}</h2>
    <p>{movie.release_date}</p>
  </div>

  <a href={'/movie/' +movie.id}>
    <img src={'https://image.tmdb.org/t/p/w500' + movie.poster_path} alt={movie.title} />
  </a>
</div>

<style>
  img{
    width: 150px;
    height: 215px;
    object-fit: cover;
    border-radius: 1rem;
    align: center;
    display: block;
    margin-left: auto;
    margin-right: auto;
    margin-bottom: 1rem;
  }
  h2{
    font-size: 20px;
    text-align: center;
    margin-bottom: 1rem;
  }
  p{
    font-size: 10px;
    text-align: center;
    margin-bottom: 1rem;
  }
</style>