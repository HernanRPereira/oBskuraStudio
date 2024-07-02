<template>
  <div class="back">
    <div class="home">
      <header>
        <div class="menu">
          <DropdownMenu />
        </div>
        <div class="header-content">
          <HeaderComponent />
        </div>
      </header>
      <div class="container">
        <h2>MACRATA</h2>
      </div>
    </div>
  </div>
</template>

<script>
import DropdownMenu from './components/Menu.vue';
import HeaderComponent from './components/HeaderComponent.vue';

export default {
  name: 'App',
  components: {
    DropdownMenu,
    HeaderComponent,
  },
};
</script>

<style>
/* Puedes agregar estilos globales aquí */
*{
  border: solid 1px black;
  margin: 0;
  padding: 0;
}

.back {
  background-image: url('./assets/milad.jpg'); /* Reemplaza 'tu-imagen.jpg' con el nombre de tu imagen */
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  width: 100vw;
  height: 100vh;
}

.home{
  padding: 2em;
}

header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.menu {
  width: 20vh;
  align-self: flex-start;
}
.header-content {
  flex: 1;
  display: flex;
  justify-content: center;
}

.container{
  height: 75vh;
  display: flex;
  align-items: center;
}

h2{
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  font-size: 5rem;
  margin: 1em;

}

</style>
