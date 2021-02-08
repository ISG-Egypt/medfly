<template>
  <div>
    <Nuxt />
  </div>
</template>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Tajawal:wght@200&display=swap');
  
  .font-tajawal {
    font-family: 'Tajawal', sans-serif;
  }
  
</style>
<script>
  export default {
    head () {
      return {
          links: [
            { 
              href: "https://fonts.googleapis.com/css2?family=Tajawal:wght@200&display=swap"
            },
            {
              href: "https://fonts.gstatic.com",
              rel:"preconnect"
            }
          ]
        }
      }
  }
</script>