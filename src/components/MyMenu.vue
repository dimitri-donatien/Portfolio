<template>
  <nav class="navigation md:justify-end">
    <ul class="menu">
      <li class="li">
        <a href="#accueil">Accueil</a>
      </li>
      <li class="li">
        <a href="#portfolio">Portfolio</a>  
      </li>
      <li class="li">
        <a href="#propos">À propos</a> 
      </li>
      <li class="li">
        <a href="#infos">Infos</a>
      </li>
    </ul>
  </nav>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'MyMenu'
}
</script>

<style lang="scss" scoped>
  .navigation {
    position: absolute;
    top: 0;
    right: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
    padding: 1rem;
  }

  .menu { 
    display: flex;
  }

  .li {
    margin: 0 12px;
  }

  .menu a {
    position: relative;
    display: inline-block;
    color: white;
    transition: color .2s ease;
    margin-bottom: 15px;
  }

  .menu a:hover {
      color: #aaa;
  }

  .menu a:hover::after,
    .menu a:hover::before {
      width: 100%;
      left: 0;
  }

  .menu a::after,
    .menu a::before {
      content: ''; 
      position: absolute;
      top: calc(100% + 5px);
      width: 0;
      right: 0;
      height: 3px;
  }

  .menu a::before {
    transition: width .4s cubic-bezier(0.51, 0.18, 0, 0.88) .1s;
    background: #2196f3;
  }

  .menu a::after {
    transition: width .2s cubic-bezier(0.29, 0.18, 0.26, 0.83);
    background: #F44336;
  }

</style>