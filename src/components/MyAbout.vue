<template>
  <section id="propos" class="flex flex-col items-center justify-center min-h-screen w-full p-4">
    <div class="w-11/12">
      <h2 class="font-bold text-3xl mb-8 md:mb-6 md:text-4xl">À propos<span class="text-blue-600">_</span></h2>
      <p>Bonjour! Je m’appelle <span class="link">Dimitri Donatien</span>, je suis <span class="link">concepteur développeur d'applications</span>, motivé, curieux et passionné par l'UI / UX et le développement. Ma spécialité est de construire des projets web de A à Z, en commençant par la définition du produit pour répondre au mieux aux besoins, en passant par la conception de l'outil, l'intégration des pages et le développement des différentes fonctionnalités. Sans oublier l'optimisation du référencement naturel et la mise en ligne. Je peux donc vous accompagner sur toutes les étapes de votre projet digital. Pour toute question, n’hésitez pas à me contacter : <a class="link" href="mailto:donatien.dim@gmail.com">donatien.dim@gmail.com</a>.</p>
    </div>
  </section>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'MyAbout'
}
</script>

<style lang="scss" scoped>

.link {
  position: relative;
  text-decoration: none;
  display: inline-block;
  color: black;
  padding: 0 1px;
  transition: color ease 0.3s;
  
}

.link::before, .link::after {
    content: '';
    position: absolute;
    background-color: rgb(248, 113, 113);
    z-index: -1;
    height: 5%;
  }

.link::before {
    width: 0%;
    left: 0;
    bottom: 0;
    transition: width ease 0.4s;
  }

.link::after {
    width: 100%;
    left: 0;
    bottom: 0;
    transition: all ease 0.6s;
  }

.link:hover::before {
      width: 100%;
    }

.link:hover::after {
      left: 100%;
      width: 0%;
      transition: all ease 0.2s;
    }


</style>