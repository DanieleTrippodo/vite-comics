<!-- Qui va la logica del componente (Vue3 + Javascript) -->
<script>
export default {
  name: 'MainHeader'
};
</script>



<!-- Qui va il contenuto di questo elemento (HTML) -->
<template>
  <header>
    <!-- Logo DC -->
    <div class="logo">
      <img src="/src/assets/img/dc-logo.png" alt="DC Logo">
    </div>

    <!-- lista link -->
    <nav>
      <ul>
        <li>CHARACTERS</li>
        <li>COMICS</li>
        <li>MOVIES</li>
        <li>TV</li>
        <li>GAMES</li>
        <li>COLLECTIBLES</li>
        <li>VIDEOS</li>
        <li>FANS</li>
        <li>NEWS</li>
        <li>SHOP</li>
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