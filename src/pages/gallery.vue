<template>
  <q-page>
    <div class="row">
      <div class="col-xs-10 offset-xs-1  q-mt-xl">
        <div class="text-center q-display-2 text-primary text-bold featured-header uppercase">Gallery</div>
      </div>
      <div class="col-lg-4 offset-lg-4 col-xs-8 offset-xs-2 q-mt-sm q-mb-xl">
        <hr>
      </div>
      <div class="col-12 q-mb-xl q-mt-md" v-for="(section, id) in gallerySection" :key="id">
        <div class="row">
          <div class="col-xs-10 offset-xs-1  q-mt-xs">
            <div class="text-center q-display-1 text-secondary text-bold featured-header uppercase"> {{ section.title }}</div>
          </div>
          <div class="col-lg-2 offset-lg-5 col-xs-8 offset-xs-2 q-mt-sm q-mb-md">
            <hr>
          </div>
          <div class="col-12">
            <div class="row flex justify-around round-borders">
              <div class="album col-lg-3 q-card q-ma-md flex justify-center items-center border-prim" v-for="(gallery, id) in section.galleries" :key="id" :style="{ backgroundImage : 'url('+ gallery.backgroundImg + ')'}" >
                <div class="col-10" style="z-index: 2">
                  <div class="q-headline text-center text-primary" >{{ gallery.title }}</div>
                </div>
                <div class="col-lg-5"><a :href="gallery.url" rel="noopener" target="_blank"><q-btn class="full-width" label="Go to album" icon="link" style="z-index: 2" color="primary" /></a></div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </q-page>
</template>

<script>
export default {
  name: 'PageGallery',
  data () {
    return {
      gallerySection: [
        {
          title: 'Glimpse of 2018',
          galleries: [
            {
              title: 'Force on duty in Un Mission in DR Congo',
              url: 'https://www.facebook.com/media/set/?set=a.1627809300643719.1073741894.629471567144169&type=1&l=b48a0571db',
              backgroundImg: '../statics/bpwn/images/facebook-gallery-2018-1.jpg'
            }
          ]
        },
        {
          title: 'Glimpse of 2017',
          galleries: [
            {
              title: 'Int. Women & Law Enforcement Conference 2017 in Australia',
              url: 'https://www.facebook.com/media/set/?set=a.1473643349393649.1073741893.629471567144169&type=1&l=fbe490ce69',
              backgroundImg: '../statics/bpwn/images/facebook-gallery-2017-1.jpg'
            },
            {
              title: 'Addl SP Mahfuza placed 3rd position in Teaching Session,Srilanka',
              url: 'https://www.facebook.com/media/set/?set=a.1431330860291565.1073741891.629471567144169&type=1&l=238776f69c',
              backgroundImg: '../statics/bpwn/images/facebook-gallery-2017-2.jpg'
            },
            {
              title: 'Al-Beli Afifa, Addl SP, DMP completed Humphrey Fellowship in USA',
              url: 'https://www.facebook.com/media/set/?set=a.1451643918260259.1073741892.629471567144169&type=1&l=e41e2d1473',
              backgroundImg: '../statics/bpwn/images/facebook-gallery-2017-3.jpg'
            },
            {
              title: 'End of the Journey of BANFPU-2(Rotation 6) MINUSTAH, HAITI',
              url: 'https://www.facebook.com/media/set/?set=a.1411020505655934.1073741889.629471567144169&type=1&l=4c6d061287',
              backgroundImg: '../statics/bpwn/images/facebook-gallery-2017-4.jpg'
            },
            {
              title: 'Visit of Hon\'ble IGP of BANFPU2, MINUSTAH at Haiti',
              url: 'https://www.facebook.com/media/set/?set=a.1377151869042798.1073741888.629471567144169&type=1&l=caf56babac',
              backgroundImg: '../statics/bpwn/images/facebook-gallery-2017-5.jpg'
            },
            {
              title: 'Australia Awards South and West Asia Short Course Award, 2017',
              url: 'https://www.facebook.com/media/set/?set=a.1359397827484869.1073741885.629471567144169&type=1&l=6c7d055328',
              backgroundImg: '../statics/bpwn/images/facebook-gallery-2017-6.jpg'
            },
            {
              title: 'Countering Violent Extremism organised by Macquaire University',
              url: 'https://www.facebook.com/media/set/?set=a.1360163694074949.1073741886.629471567144169&type=1&l=9baad37948',
              backgroundImg: '../statics/bpwn/images/facebook-gallery-2017-7.jpg'
            },
            {
              title: 'Taptun Zaman, SP, working as Policy Officer at UN HQ',
              url: 'https://www.facebook.com/media/set/?set=a.1172469039511083.1073741854.629471567144169&type=1&l=1d6f3da1d2',
              backgroundImg: '../statics/bpwn/images/facebook-gallery-2017-8.jpg'
            },
            {
              title: 'UN Medal Parade Ceremony of BANFPU2, MINUSTAH at Haiti',
              url: 'https://www.facebook.com/media/set/?set=a.1346202928804359.1073741883.629471567144169&type=1&l=08dbfe3721',
              backgroundImg: '../statics/bpwn/images/facebook-gallery-2017-9.jpg'
            },
            {
              title: 'Detective Fatema Begum, Addl IG, Issue April, 2017',
              url: 'https://www.facebook.com/media/set/?set=a.1416675058423812.1073741890.629471567144169&type=1&l=b0b4d3591a',
              backgroundImg: '../statics/bpwn/images/facebook-gallery-2017-10.jpg'
            },
            {
              title: 'Joint exercise in Haiti with BANFPU2, India and Senegal',
              url: 'https://www.facebook.com/media/set/?set=a.1305506839540635.1073741880.629471567144169&type=1&l=1e984886ef',
              backgroundImg: '../statics/bpwn/images/facebook-gallery-2017-11.jpg'
            },
            {
              title: '5th Gender Protection in Peace Operations\' Course in Italy',
              url: 'https://www.facebook.com/media/set/?set=a.1342387422519243.1073741882.629471567144169&type=1&l=3a5444d77c',
              backgroundImg: '../statics/bpwn/images/facebook-gallery-2017-12.jpg'
            },
            {
              title: 'UN Medal Parade of BANFPU1, at Congo',
              url: 'https://www.facebook.com/media/set/?set=a.1351742951583690.1073741884.629471567144169&type=1&l=a2af6c254d',
              backgroundImg: '../statics/bpwn/images/facebook-gallery-2017-13.jpg'
            },
            {
              title: 'Hubert H. Humphrey Fellowship Program 2016-2017 in USA',
              url: 'https://www.facebook.com/media/set/?set=a.1236428149781838.1073741876.629471567144169&type=1&l=9d53f2ddc8',
              backgroundImg: '../statics/bpwn/images/facebook-gallery-2017-14.jpg'
            },
            {
              title: 'UN Military Units Manual Implementation Regional Seminar',
              url: 'https://www.facebook.com/media/set/?set=a.1230550717036248.1073741875.629471567144169&type=1&l=94b089fbf6',
              backgroundImg: '../statics/bpwn/images/facebook-gallery-2017-15.jpg'
            }
          ]
        }
      ]
    }
  }
}
</script>

<style scoped>
  .album {
    height: 300px;
    background-size: 100% 100%;
    position: relative;
  }

  .album:after {
    content: '';
    background: rgba(48, 51, 107, 0.85);
    height: 100%;
    width: 100%;
    position: absolute;
    top: 0;
    z-index: 0;
    border-radius: 2px;
  }

</style>
