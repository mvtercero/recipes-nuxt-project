<template>
  <header>
    <nav>
      <ul>
        <li>
          <nuxt-link to="/">Inicio</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/recipes">Recetas</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/about">Sobre nosotros</nuxt-link>
        </li>
      </ul>
    </nav>
  </header>
</template>

<style scoped>
header {
  width: 100%;
  height: 30px;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #5289;
}

ul {
  list-style: none;
  margin: 0;
  padding: 0;
  display: flex;
  justify-content: center;
  align-items: center;
}

li {
  margin: 0 10px;
}

a {
  text-decoration: none;
  color: white;
}
</style>
