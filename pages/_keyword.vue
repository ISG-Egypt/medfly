<template>
  <div class="font-tajawal">
    <SectionFull classes="relative">
      <!-- main -->
        <img class="absolute top-0 left-0" style="max-width: 220px;" src="~/assets/images/logo.svg" title="MedFly logo" />
        <div 
          class="bg-vd-purple"
          style="width: 100%"
          
        >
          <div 
          
            class="block header-photo"
            :style="{
              width: '100%',
              overflow: 'hidden',
              backgroundImage: `url(${mainBackgroundUrl})`,
              backgroundPosition: main_background_position ? main_background_position : 'unset'
            }"
            
          > 
            <!-- <div class="relative" style="width: 100%; overflow: hidden;">
             <img class="absolute w-full h-full" src="~/assets/images/bg-first.jpg" />
            </div> -->
          </div>
          <div 
          
            class="block header-cta pb-20 md:pb-0 flex flex-col md:flex-row"
            :style="{
              direction: 'rtl',
              backgroundImage: `url(${ctaBackgroundUrl})`,
            }"
            
          > 
            
            <div class="w-full md:w-8/12 flex flex-col items-center md:justify-start md:items-center my-4 mt-12 text-center" :style="{
                direction: 'rtl',
                color: cta_text_color_light ? '#FFF' : '#000'
              }">
              <span class="text-4xl font-bold">{{ heading }}</span>
              <span class="text-3xl font-bold" v-html="subtitle"></span>
            </div>

            <div class="w-full md:w-6/12 flex items-center justify-center">
            <button 
                :class="['px-8 py-4 text-white text-2xl rounded flex items-center justify-between',
                  cta_text_color_light ?  '': 'bg-vd-purple'
                ]"
                :style="{
                  minWidth: '240px',
                  backgroundColor: cta_text_color_light ? '#bf697b' : ''
                }"
                
                @click="goTo('WHATSAPP')"
              >
                <span>إحجز الآن</span>
                <!-- <svg t="1612610948782" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="2108" width="20" height="20"><path d="M427.52 955.733333a17.066667 17.066667 0 0 1-15.837867-10.7008l-171.52-426.666666a17.1008 17.1008 0 0 1 0-12.731734l171.52-426.666666a17.066667 17.066667 0 0 1 31.675734 12.731733L274.397867 512l168.96 420.3008A17.066667 17.066667 0 0 1 427.52 955.733333zM768 955.733333H597.333333c-6.980267 0-13.2608-4.266667-15.854933-10.752l-169.8304-426.666666a17.134933 17.134933 0 0 1 0-12.612267l169.8304-426.666667A17.066667 17.066667 0 0 1 597.333333 68.266667h170.666667a17.083733 17.083733 0 0 1 15.854933 23.3984L615.714133 512l168.1408 420.334933A17.066667 17.066667 0 0 1 768 955.733333z m-159.0784-34.133333h133.888l-161.314133-403.2512a17.134933 17.134933 0 0 1 0-12.680533L742.792533 102.4h-133.888l-163.037866 409.6 163.054933 409.6z" p-id="2109" fill="#FFF"></path></svg> -->
                <svg t="1613323734200" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="2108" width="25" height="25"><path d="M700.8 592.7c-28.5-16-61.6-31.3-82.4-37.7-20.8-6.4-47.7 44.5-47.7 44.5s-25.2 6.1-80.6-38c-55.4-44.1-61-83.6-61-83.6s28.5-25.1 28.5-42.6-11.5-53.2-33.1-84.4c-21.6-31.2-114.7 0-87.8 111.7 10.2 42.3 33.1 87.4 112.4 155.8s154 77.5 200.1 69.2c46.2-8.3 80.1-78.9 51.6-94.9z" fill="#6ED65B" p-id="2109"></path><path d="M516.5 112.3c-218.5 0-395.6 174.9-395.6 390.6 0 77.3 22.8 149.4 62 210.1 5 7.7-76.6 194.1-70.6 198.7 3.5 2.7 204.5-71.5 208-69.5 57.8 32.7 124.8 51.4 196.2 51.4 218.5 0 395.6-174.9 395.6-390.6 0-215.8-177.1-390.7-395.6-390.7z m0 703.1c-63 0-121.8-18.2-171.1-49.6-7-4.5-124.6 45.4-126.9 43.6-2.8-2.1 44.2-119.8 41.6-123.4-37.8-51.5-60-114.8-60-183.2 0-172.6 141.7-312.5 316.5-312.5s316.5 139.9 316.5 312.5c-0.2 172.7-141.8 312.6-316.6 312.6z" fill="#6ED65B" p-id="2110"></path></svg>
              </button>
            </div>


          </div>
        </div>
        <div>

        </div>

        <!-- 
          
          INITIAL REQUEST 

          <div class="back-image" :style="{
            backgroundImage: 'url(\'~assets/images/bg-2.jpg\')',
          }"></div>
        <div class="overlay"></div>
        <div 
          class="relative w-3/4 md:w-full"
          style="max-width: 320px;"
        >
            <img src="~/assets/images/logo.svg" title="MedFly logo" />
        </div>

        <div class="back-text">
            <div>
              <h1 class="text-3xl md:text-5xl pb-4 ">ازالة الشعر بالليزر</h1>
              <div class="flex flex-col text-md md:text-3xl mb-8">
                <span></span>
                <span>أسعار تبدأ من ١٥٠ جنيه للجلسة</span>
              </div>
              <button 
                style="min-width: 200px"
                class="flex justify-between items-center bg-l-pink text-vd-purple rounded px-4 py-2 shadow-lg shadow-vd-purple" 
              >
                <span class="text-xl">إحجز الآن</span>
                <svg t="1612610948782" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="2108" width="20" height="20"><path d="M427.52 955.733333a17.066667 17.066667 0 0 1-15.837867-10.7008l-171.52-426.666666a17.1008 17.1008 0 0 1 0-12.731734l171.52-426.666666a17.066667 17.066667 0 0 1 31.675734 12.731733L274.397867 512l168.96 420.3008A17.066667 17.066667 0 0 1 427.52 955.733333zM768 955.733333H597.333333c-6.980267 0-13.2608-4.266667-15.854933-10.752l-169.8304-426.666666a17.134933 17.134933 0 0 1 0-12.612267l169.8304-426.666667A17.066667 17.066667 0 0 1 597.333333 68.266667h170.666667a17.083733 17.083733 0 0 1 15.854933 23.3984L615.714133 512l168.1408 420.334933A17.066667 17.066667 0 0 1 768 955.733333z m-159.0784-34.133333h133.888l-161.314133-403.2512a17.134933 17.134933 0 0 1 0-12.680533L742.792533 102.4h-133.888l-163.037866 409.6 163.054933 409.6z" p-id="2109" fill="#2b151e"></path></svg>
              </button>
            </div>
        </div> -->
    </SectionFull>
    <section class="flex flex-col md:flex-row md:justify-around bg-white md:py-20">
      <div class="flex w-full md:w-5/12 justify-center items-center">
        <iframe class="video" src="https://drive.google.com/file/d/1W6L4WNSVpVqHcCScnyr4pATJPdZN7sFq/preview"></iframe>
      </div>
      <div class="flex w-full md:w-4/12 justify-center items-center mb-20 mt-20 md:mt-0 text-center md:mb-0">
        <p class="text-3xl text-center font-bold">
          مركز عيادات الصحة والجمال  <br>في قلب القاهرة الجديدة
        </p>
        <!-- <ul class="text-3xl text-right">
          <li>غرف مريحة</li>
          <li>في قلب التجمع الخامس</li>
          <li>متعددة التخصصات</li>
          <li>عيادات الصحة والجمال</li>
        </ul> -->
      </div>
    </section>
    <div class="flex flex-col md:flex-row">
      <button class="cta-button" @click="goTo('FACEBOOK')">
        <svg t="1612613760758" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="3694" width="40" height="40"><path d="M790.924 294.479h-84.491v-50.5c0-68.095-55.399-123.495-123.495-123.495H443.944c-68.095 0-123.495 55.399-123.495 123.495v50.5h-86.99c-50.729 0-92 41.271-92 92V751.95c0 50.729 41.271 92 92 92h557.465c50.729 0 92-41.271 92-92V386.479c0-50.729-41.272-92-92-92z m-414.475-50.501c0-37.217 30.278-67.495 67.495-67.495h138.994c37.217 0 67.495 30.278 67.495 67.495v48.997H376.449v-48.997zM826.924 751.95c0 19.851-16.149 36-36 36H233.458c-19.851 0-36-16.149-36-36V386.479c0-19.851 16.149-36 36-36h557.465c19.851 0 36 16.149 36 36V751.95z" p-id="3695"></path><path d="M631.684 542.966h-92.245V450.72c0-14.497-11.752-26.249-26.249-26.249-14.497 0-26.249 11.752-26.249 26.249v92.245h-92.245c-14.497 0-26.249 11.752-26.249 26.249s11.752 26.249 26.249 26.249h92.245v92.245c0 14.497 11.752 26.249 26.249 26.249 14.497 0 26.249-11.752 26.249-26.249v-92.245h92.245c14.497 0 26.249-11.752 26.249-26.249s-11.752-26.248-26.249-26.248z" p-id="3696"></path></svg>
        <span>حالات سابقة</span>
      </button>
      <button class="cta-button cta-map-bg" @click="goTo('ADDRESS')">
        <svg t="1612614039434" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="6702" width="40" height="40"><path d="M511.717567 127.981836c34.606169 0 68.116377 6.704702 99.598393 19.928889 30.468942 12.797467 57.817824 31.142278 81.289398 54.525847 48.328705 48.146557 74.943876 112.571868 74.943876 181.406606 0 37.119409-7.90504 79.557964-23.496134 126.136816-14.530948 43.412742-35.730783 90.39273-63.010079 139.63627-58.604746 105.791441-129.349997 194.2184-169.326477 240.706177C471.734948 843.819315 400.986627 755.37496 342.395184 649.616264c-27.282367-49.244564-48.484248-96.225575-63.017242-139.63627-15.59314-46.578852-23.499204-89.017406-23.499204-126.135792 0-68.834738 26.616194-133.26005 74.9449-181.406607 23.471574-23.38357 50.821479-41.72838 81.291444-54.525847 31.483038-13.225209 64.99427-19.929912 99.602485-19.929912m0-63.956637c-176.35966 0-319.794443 141.665487-319.794443 319.817979 0 186.559976 159.91206 420.09073 276.493242 554.182728 0.435928 0.523933 19.150152 21.444405 42.284035 21.444405h2.029216c23.134907 0 41.84299-20.924565 42.289152-21.444405 116.605741-134.093021 276.489148-367.627868 276.489149-554.182728-0.001023-178.152493-143.43683-319.817979-319.790351-319.817979z" p-id="6703"></path><path d="M511.706311 319.863005c35.270295 0 63.964824 28.694529 63.964824 63.964824s-28.694529 63.964824-63.964824 63.964824-63.964824-28.694529-63.964824-63.964824 28.694529-63.964824 63.964824-63.964824m0-63.956638c-70.64906 0-127.921461 57.272401-127.921461 127.921462s57.272401 127.921461 127.921461 127.921461 127.921461-57.272401 127.921461-127.921461-57.272401-127.921461-127.921461-127.921462z" p-id="6704"></path></svg>
        <span>عناوين الفروع</span>
      </button>
      <button class="cta-button" style="background-color: #ebffcb" @click="goTo('WHATSAPP')">
        <svg t="1612613966632" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="5594" width="40" height="40"><path d="M784.128 240.128A380 380 0 0 0 513.6 128C302.88 128 131.2 299.52 131.2 510.24a380.224 380.224 0 0 0 51.008 191.136L128 899.488l202.752-53.248a382.656 382.656 0 0 0 182.72 46.624h0.16c210.752 0 382.24-171.488 382.368-382.368 0-102.112-39.744-198.112-111.872-270.4zM513.6 828.256h-0.128a317.76 317.76 0 0 1-161.76-44.256l-11.616-6.88-120.384 31.52 32.128-117.28-7.488-12a316.928 316.928 0 0 1-48.64-169.12c0-175.104 142.624-317.6 318.016-317.6a315.616 315.616 0 0 1 224.64 93.12 316 316 0 0 1 92.96 224.736c0 175.264-142.624 317.76-317.76 317.76z m174.24-238.016c-9.504-4.736-56.512-27.84-65.248-30.976-8.736-3.264-15.136-4.768-21.504 4.736-6.4 9.6-24.64 31.136-30.24 37.504-5.504 6.24-11.136 7.136-20.64 2.368-9.6-4.736-40.352-14.88-76.864-47.488-28.384-25.28-47.616-56.64-53.12-66.144-5.632-9.6-0.64-14.72 4.128-19.52 4.352-4.224 9.6-11.104 14.368-16.736 4.736-5.472 6.4-9.472 9.6-15.872 3.136-6.368 1.536-12-0.864-16.736-2.368-4.736-21.472-51.872-29.472-71.008-7.776-18.624-15.648-16-21.504-16.352-5.504-0.256-11.872-0.256-18.24-0.256-6.4 0-16.768 2.368-25.536 12-8.736 9.504-33.376 32.64-33.376 79.616 0 47.008 34.24 92.48 39.04 98.88 4.736 6.24 67.36 102.72 163.2 144.128 22.784 9.856 40.512 15.744 54.4 20.128 22.88 7.232 43.744 6.24 60.256 3.84 18.368-2.72 56.48-23.104 64.48-45.472 7.904-22.24 7.904-41.376 5.504-45.376-2.368-4-8.736-6.4-18.368-11.264z" p-id="5595"></path></svg>
        <span>للحجز والإستعلام</span>
      </button>
    </div>
  </div>
</template>

<script>


const keywords = {
  default: 'laser-hair-removal',
  'laser-hair-removal': {
    heading: 'إزالة الشعر بالليزر',
    subtitle: 'تمتعي بنعومة دائمة',
    whatsapp: 'ازالة الشعر بالليزر',
  },
  'brazillian-bottom': {
    heading: 'المؤخرة البرازيلية',
    subtitle: 'إنت أحلى منهم',
    whatsapp: 'المؤخرة البرازيلية',
    cta_bg: 'cta-bgav.jpg',
    cta_text_color_light: true 

  },
  'hair-implant': {
    heading: 'زراعة الشعر',
    subtitle: 'رجع لحظة حلوة في يوم عشتها',
    whatsapp: 'زراعة الشعر',
    cta_bg: 'cta-bghair-implant.jpg'
  },
  'botox': {
    heading: 'وداعا للتجاعيد مع البوتكس',
    subtitle: 'في خلال ١٥ دقيقة',
    whatsapp: 'بوتكس',
    cta_bg: 'cta-bgav.jpg',
    cta_text_color_light: true 
  },
  'filler': {
    heading: 'فيلر كولاجين',
    subtitle: 'نتائج رائعة وسريعة',
    whatsapp: 'فيلر',
    cta_bg: 'cta-bgav.jpg',
    cta_text_color_light: true 
  },
  'sleeve-gastrec': {
    heading: 'تكميم معده',
    subtitle: 'عشان نساعدك تخس',
    whatsapp: 'فيلر',
    cta_bg: 'cta-bgav.jpg',
    cta_text_color_light: true 
  },
  'after-valentines': {
    heading: 'فاجئها بهدية تانية',
    subtitle: 'اسعار تبدأ من ٣٠٠ جنيه', 
    whatsapp: 'هدية لبعد الفلانتاين',
    main_bg: 'BG-MAIN.jpg',
    main_background_position: 'bottom',
    cta_bg: 'cta-bgav.jpg',
    cta_text_color_light: true
  },
  

}

export default {
    created () {
      
      this.keyword = this.$route.params.keyword

      
      if (!this.keyword) return
      if (keywords[this.keyword] === undefined) return 
      
      this.heading = keywords[this.keyword].heading
      this.subtitle = keywords[this.keyword].subtitle
      this.whatsapp = keywords[this.keyword].whatsapp
      
      if (keywords[this.keyword].cta_bg) this.cta_bg = keywords[this.keyword].cta_bg
      if (keywords[this.keyword].main_bg) this.main_bg = keywords[this.keyword].main_bg
      if (keywords[this.keyword].cta_text_color_light) this.cta_text_color_light = keywords[this.keyword].cta_text_color_light
      if (keywords[this.keyword].main_background_position) this.main_background_position = keywords[this.keyword].main_background_position
      
    },
    data () {
      return {
        keyword: undefined,
        images_folder: '~/assets/images/',
        heading: keywords[keywords.default].heading,
        subtitle: keywords[keywords.default].subtitle,
        whatsapp: keywords[keywords.default].whatsapp,
        main_bg: undefined,
        main_background_position: undefined,
        cta_bg: keywords[keywords.default].cat_bg,
        cta_text_color_light: false
      }
    },
    methods: {
      goTo (place) {

        const places = {          
          WHATSAPP: 'https://wa.me/201101740224?text='+encodeURI('لوسمحت عندي استفسار بخصوص ' + this.whatsapp),
          ADDRESS: 'https://goo.gl/maps/cMfQEU3RqD6rqQwk8',
          FACEBOOK: 'https://www.facebook.com/Medfly-clinic-112243000690582'
        }

        window.open(places[place])
      }
    },
    computed: {
      ctaBackgroundUrl () {
        return '/' + (this.cta_bg || 'cta-bg.jpg')
      },
      mainBackgroundUrl () {
        return '/' + (this.main_bg || 'bg-first.jpg')
      }
    }
    
  }
</script>

<style>
/* Sample `apply` at-rules with Tailwind CSS
.container {
@apply min-h-screen flex justify-center items-center text-center mx-auto;
}
*/

    /* section {
        min-width: 100vw; 
        min-height: 100vh; 
        @apply bg-vl-pink;
    } */

  .cta-button {
    @apply px-8 py-8;
    @apply border flex-grow flex items-center justify-between; 
    @apply text-3xl;
  }

  .main {
    /* background-image: url('~assets/images/bg2.jpg'); */
    background-size: cover;
    background-position: top;
    background-repeat: no-repeat;
  }

  .back-image {
    z-index: -1;
    @apply absolute top-0 left-0 w-full h-full;
  }

  .back-text {
    z-index: 0;
    direction: rtl;
    @apply flex-grow flex items-center p-20;
  }

  .overlay {
    z-index: 0;
    background: rgba(255,255,255,0.94);
    @apply absolute top-0 left-0 w-full h-full;
  }

  .video {
    width: 100%;
    height: 33%;
    min-height: 291px;
  }

  .header-photo {
    background-image: url('~assets/images/bg-first.jpg');
    min-height: 80vh;
    max-height: 80vh;
    background-size: cover;
    border-bottom: 3px solid #29151e;
  }

  .header-cta { 
    /* background-image: url('~assets/images/cta-bg.jpg'); */
    min-height: 20vh;

    background-position: center;
    background-size: cover;
  }

  .cta-map-bg {
     background-image: url('~assets/images/map.jpg')
  }

  @media screen (min-width: 300px) {

  }

</style>
