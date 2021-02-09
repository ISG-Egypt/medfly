<template>
  <div>
    <Nuxt />
  </div>
</template>

<style>

  /* arabic */
  @font-face {
    font-family: 'Tajawal';
    font-style: normal;
    font-weight: 200;
    font-display: swap;
    src: url(https://fonts.gstatic.com/s/tajawal/v3/Iurf6YBj_oCad4k1l_6gHrRpiZtK6GwN9w.woff2) format('woff2');
    unicode-range: U+0600-06FF, U+200C-200E, U+2010-2011, U+204F, U+2E41, U+FB50-FDFF, U+FE80-FEFC;
  }
  /* latin */
  @font-face {
    font-family: 'Tajawal';
    font-style: normal;
    font-weight: 200;
    font-display: swap;
    src: url(https://fonts.gstatic.com/s/tajawal/v3/Iurf6YBj_oCad4k1l_6gHrFpiZtK6Gw.woff2) format('woff2');
    unicode-range: U+0000-00FF, U+0131, U+0152-0153, U+02BB-02BC, U+02C6, U+02DA, U+02DC, U+2000-206F, U+2074, U+20AC, U+2122, U+2191, U+2193, U+2212, U+2215, U+FEFF, U+FFFD;
  }

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