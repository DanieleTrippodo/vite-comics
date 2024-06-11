<!-- Qui va la logica del componente (Vue3 + Javascript) -->
<script>
export default {
  name: 'ComicList',
  data() {
    return {
      comics: []
    };
  },
  created() {
    fetch('/dc-comics.json')
      .then(response => response.json())
      .then(data => {
        this.comics = data;
      });
  }
}
</script>



<!-- Qui va il contenuto di questo elemento (HTML) -->
<template>

  <h2 class="TitleSeriesCard">Current Series</h2>


   <div class="comic-list">
    <div v-for="comic in comics" :key="comic.series" class="comic-card">

      <!-- aggiunta delle copertine -->
      <img :src="comic.thumb" :alt="comic.series" class="comic-image" />


    </div>
  </div>
</template>



<!-- Qui va lo stile CSS di questo elemento (CSS) -->
<style scoped lang="scss">
.comic-list {
  display: flex;
  flex-wrap: wrap;
  gap: 1rem;
  justify-content: center;
  background-color: #1c1c1c;
}


/* Lista fumetti */
.comic-card {
  overflow: hidden;  /* si usa quando il contenuto è più grande del contenitore, per nascondere l'elemento che esce fuori */
  width: 250px;
  height: 15rem;

  color: white;  /* il clore del titolo del fumetto */
  padding: 1.4rem;

  margin-top: 1rem;
  margin-bottom: 3rem;
}

/* Copertina del fumetto */
.comic-image {
  width: 100%;
  height: auto;
}

/* Titolo Fumetto */
.comic-title {
  font-size: 1.2rem;
  margin: 0.5rem 0;
}


.TitleSeriesCard{
  background-color: #007bff;
  color: white;
  padding: 1rem;


  font-size: 2.6rem;
  padding-left: 3rem;
  padding-right: 3rem;

  display: inline;
  margin-left: 1.9rem;
}
</style>