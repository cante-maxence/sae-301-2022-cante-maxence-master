<template>

  <main class="bg-black  p-5 bg-gradient-to-b from-[#080038] to-black ...">




    <header class="">
      <router-link class="logo" to="/"> TiK•TaK</router-link>
      <div class="menu-toggle"></div>
      <nav>
        <ul>

          <li>
            <router-link to="/">Accueil</router-link>
          </li>

          <li>
            <router-link to="/connexion">Connexion / Inscription</router-link>
          </li>
          <li>
            <router-link to="/liste">Liste</router-link>
          </li>

        </ul>
      </nav>
      <div class="clearfix"></div>
    </header>


    <!-- Affiche les pages -->
    <Suspense>
      <router-view class="m-2 border-2 p-2" />
    </Suspense>





  </main>
  <footer class="bg-black p-5 grid grid-cols-1 md:grid-cols-12">
    <div class="md:col-span-2 pb-2 md:mb-0">
      <p class="text-gray-200">Information</p>
      <ul class="pt-5 text-gray-400">
        <li><a href="#"> TiK•TaK</a> </li>
        <li><a href="#">Politique de confidentialité</a></li>
        <li><a href="#">Mentions légales</a></li>
        <li><a href="#">Cookies</a></li>
      </ul>
    </div>
    <div class="md:col-span-2 pb-2 md:mb-0">
      <p class="text-gray-200">Compte</p>
      <ul class="pt-5 text-gray-400">
        <li>
          <router-link to="/connexion">Connexion</router-link>
        </li>
        <li>
          <router-link to="/connexion">Inscription</router-link>
        </li>
        <li><a href="#">Mes données</a></li>
      </ul>
    </div>
    <div class="md:col-span-2 pb-2 md:mb-0">
      <p class="text-gray-200">Besoin d'aide ?</p>
      <ul class="pt-5 text-gray-400">
        <li><a href="#">F.A.Q</a></li>
        <li><a href="#">Contactez-nous</a></li>

      </ul>
    </div>
    <div class="md:col-span-2 pb-2 md:mb-0">
      <p class="text-gray-200">Nos Réseaux</p>
      <ul class="pt-5 text-gray-400">
        <li><a href="#">Facebook</a></li>
        <li><a href="#">Twitter</a></li>

      </ul>
    </div>
    <div class="md:col-span-4 pb-2 md:mb-0">

      <div class="mt-5 md:col-span-12 text-center text-gray-400 pt-2 ">
        Crée par <p class="text-2xl text-white">Maxence Cante</p> 2022
      </div>
    </div>
  </footer>


</template>

<script setup lang="ts">

</script>

<style>
header {
  position: relative;
  max-width: 1200px;
  margin: 20px auto;
  padding: 10px;
  background: #fff;
  box-sizing: border-box;
  border-radius: 4px;
  box-shadow: 0 2px 5px rgba(0, 0, 0, .8);

}

.logo {
  color: #080038;
  height: 60px;
  font-size: 36px;
  line-height: 60px;
  padding: 0 20px;
  text-align: center;
  box-sizing: border-box;
  float: left;
  font-weight: 700;
  text-decoration: none;
}

nav {
  float: right;
}

.clearfix {
  clear: both;
}

nav ul {
  margin: 0;
  padding: 0;
  display: flex;
}

nav ul li {
  list-style: none;
}

nav ul li a {
  display: block;
  margin: 10px 0;
  padding: 10px 20px;
  text-decoration: none;
  color: #262626;
}

nav ul li a.active,
nav ul li a:hover {
  background: #080038;
  color: #fff;
  transition: 0.5s;
}

@media(max-width: 1200px) {
  header {
    margin: 20px;
  }
}

@media(max-width: 768px) {
  .menu-toggle {
    display: block;
    width: 40px;
    height: 40px;
    margin: 10px;
    float: right;
    cursor: pointer;
    text-align: center;
    font-size: 30px;
    color: #069370;
  }

  .menu-toggle:before {
    content: '\f0c9';
    font-style: fontAwesome;
    line-height: 40px;
  }

  .menu-toggle.active:before {
    content: '\f00d';
  }

  nav {
    display: none;
  }

  nav.active {
    display: block;
    width: 100%;
  }

  nav.active ul {
    display: block;
  }

  nav.active ul li {
    margin: 0;
  }
}
</style>

<script>
export default {
  data() {
    return {
      isDark: true,
    };
  },
  components: {

  },
};
</script>