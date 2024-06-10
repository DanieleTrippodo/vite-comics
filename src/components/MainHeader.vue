<!-- Qui va la logica del componente (Vue3 + Javascript) -->
<script>
export default {
  name: 'MainHeader'
};
</script>



<!-- Qui va il contenuto di questo elemento (HTML) -->
<template>
  <header>
    <div class="logo">
      <img src="/src/assets/img/dc-logo.png" alt="DC Logo">
    </div>
    <nav>
      <ul>
        <li><a href="#">CHARACTERS</a></li>
        <li><a href="#">COMICS</a></li>
        <li><a href="#">MOVIES</a></li>
        <li><a href="#">TV</a></li>
        <li><a href="#">GAMES</a></li>
        <li><a href="#">COLLECTIBLES</a></li>
        <li><a href="#">VIDEOS</a></li>
        <li><a href="#">FANS</a></li>
        <li><a href="#">NEWS</a></li>
        <li><a href="#">SHOP</a></li>
      </ul>
    </nav>
  </header>
</template>



<!-- Qui va lo stile CSS di questo elemento (CSS) -->
<style scoped lang="scss">
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: #fff;
  padding: 20px;

  .logo img {
    height: 50px;
  }

  nav ul {
    list-style: none;
    display: flex;
    gap: 20px;

    li a {
      text-decoration: none;
      color: #000;
    }
  }
}
</style>