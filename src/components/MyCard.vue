<template>
    <div class="item">
      <div class="item-image">
        <img :src="image" alt="" />
      </div>
      <div class="item-text">
        <div class="item-text-wrapper">
          <p class="item-text-dek">{{ category }}</p>
          <h2 class="item-text-title">{{ title }}</h2>
        </div>
      </div>
      <a class="item-link" :href="link" target="_blank" rel="noopener noreferrer"></a>
    </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'MyCard',
  props: {
    image: String,
    category: String,
    title: String,
    link: String
  }
}
</script>

<style lang="scss" scoped>

.item {
    position: relative;
    background-color: rgba(96, 165, 250, .5);
    overflow: hidden;
  }
  .item:after {
    content: "";
    display: block;
    background-color: inherit;
    opacity: 0.9;
    width: 100%;
    height: 100%;
    position: absolute;
    top: 0;
    left: 0;
    transform: scale(2) translateX(-75%) translateY(-75%) translateZ(0) rotate(-30deg);
    transition: transform 3s cubic-bezier(0.23, 1, 0.32, 1);
  }
  .item:hover:after {
    transform: scale(2) translateX(0%) translateY(0%) translateZ(0) rotate(-30deg);
  }
  .item:hover .item-image {
    transform: scale(1.2) translateZ(0);
  }
  .item:hover .item-text {
    opacity: 1;
    transform: translateY(0);
  }
  
  .item-image {
    height: auto;
    -webkit-backface-visibility: hidden;
            backface-visibility: hidden;
    transform: translateZ(0);
    transition: transform 750ms cubic-bezier(0.23, 1, 0.32, 1);
  }
  .item-image::before {
    content: "";
    display: block;
    padding-top: 95%;
    overflow: hidden;
  }
  .item-image img {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: auto;
    line-height: 0;
  }
  
  .item-text {
    position: absolute;
    top: 0;
    right: 0;
    left: 0;
    bottom: 0;
    opacity: 0;
    text-align: center;
    z-index: 1;
    color: #ffffff;
    transition: opacity 500ms cubic-bezier(0.23, 1, 0.32, 1), transform 500ms cubic-bezier(0.23, 1, 0.32, 1);
    transition-delay: 300ms;
    transform: translateY(-20%);
  }
  
  .item-text-wrapper {
    width: 100%;
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
  }
  
  .item-text-title {
    font-weight: normal;
    padding: 0 15px;
    margin: 5px 0 0 0;
  }
  
  .item-text-dek {
    text-transform: uppercase;
    font-style: 14px;
    opacity: 0.7;
    margin: 0;
  }
  
  .item-link {
    position: absolute;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    z-index: 2;
    line-height: 0;
    overflow: hidden;
    text-indent: -9999px;
  }
</style>