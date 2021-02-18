<template>
  <footer class="background-footer">
    <!-- Copyright Bar -->
    <div class="pt-2">
        <div class="flex pb-5 px-3 m-auto pt-5 border-t border-red-600 text-white text-sm flex-col md:flex-row max-w-6xl">
            <div class="mt-2">
                © Copyright 2021-2022. All Rights Reserved.
            </div>
        </div>
    </div>
    
  </footer>
</template>

<script>
  // @ is an alias to /src

  export default {
    name: 'MyFooter'
  }
  
</script>

<style lang="scss" scoped>

  .background-footer {
    background-color: #131313;
  }

</style>