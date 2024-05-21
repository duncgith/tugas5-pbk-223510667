<template>
  <q-layout view="hHh lpR fFf">
    <q-header elevated class="bg-warning text-white" height-hint="98">
      <q-toolbar>
        <q-btn dense flat round icon="menu" @click="toggleLeftDrawer" />
        <q-toolbar-title>
          <q-avatar>
            <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTP0VK68vznWKlqF89Fx7w4Z-2nDFQihR_8z73xP5jDWQ&s">
          </q-avatar>
          DUnc fixedgear
        </q-toolbar-title>
        <q-btn dense flat round icon="menu" @click="toggleRightDrawer" />
      </q-toolbar>
      <q-tabs align="left">
        <q-route-tab to="/page1" label="HOME" />
        <q-route-tab to="/page2" label="SEARCH" />
        <q-route-tab to="/page3" label="CART" />
      </q-tabs>
    </q-header>

    <q-drawer show-if-above v-model="leftDrawerOpen" side="left" bordered>
      <div class="q-pa-md row items-start q-gutter-md">
    <q-card class="my-card">
      <img src="https://www.ausbikesports.com/cdn/shop/files/thumbnail_5034A2E5-9BB4-431E-AAD6-94FF660039A9_900x.jpg?v=1693225130">

      <q-card-section>
        <div class="text-h6">yang penting sepedaanya bukan sepedanya</div>
        <div class="text-subtitle2">by ADunc</div>
      </q-card-section>

      <q-card-section class="q-pt-none">
        {{ lorem }}
      </q-card-section>
    </q-card>

    <q-card class="my-card">
      <q-img src="https://www.static-src.com/wcsstore/Indraprastha/images/catalog/full//99/MTA-81017918/no-brand_no-brand_full01.jpg">
        <div class="absolute-bottom text-subtitle2 text-center">
          Title
        </div>
      </q-img>
    </q-card>

    <q-card class="my-card">
      <q-img src="https://superlive.id/storage/superadventure/2020/01/09/e1325fbdc695.jpg">
        <div class="absolute-bottom text-h6">
          Title
        </div>
      </q-img>

      <q-card-section>
        {{ lorem }}
      </q-card-section>
    </q-card>

    <q-card class="my-card">
      <q-img src="https://cdn.quasar.dev/img/parallax2.jpg">
        <div class="text-subtitle2 absolute-top text-center">
          Title
        </div>
      </q-img>
    </q-card>

    <q-card class="my-card">
      <q-img src="https://cdn.quasar.dev/img/parallax2.jpg">
        <div class="text-h5 absolute-bottom text-right">
          Title
        </div>
      </q-img>
    </q-card>

    <q-card class="my-card">
      <q-item>
        <q-item-section avatar>
          <q-avatar>
            <img src="https://www.lazone.id/storage/news/Juli2022/22_Juli/Sport/fixie-cover.jpg">
          </q-avatar>
        </q-item-section>

        <q-item-section>
          <q-item-label>ADunc</q-item-label>
          <q-item-label caption>trackbike athlete</q-item-label>
        </q-item-section>
      </q-item>

      <img src="https://preview.redd.it/ssn44xrzi0541.png?auto=webp&s=229d11fa6d6c731c1a0ab05be7cf157ea4062a0f">
    </q-card>

    <q-card class="my-card">
      <q-img src="https://www.fishtailcyclery.com/cdn/shop/products/CinelliVigorelliShark.jpg?v=1605986740">
        <div class="absolute-bottom">
          <div class="text-h6">cinelli VS</div>
          <div class="text-subtitle2">by fixfix</div>
        </div>
      </q-img>

      <q-card-actions>
        <q-btn flat>buy</q-btn>
        <q-btn flat>add cart</q-btn>
      </q-card-actions>
    </q-card>
  </div>
    </q-drawer>

    <q-drawer show-if-above v-model="rightDrawerOpen" side="right" bordered>
      <div class="q-pa-md row items-start q-gutter-md">
    <q-card class="my-card">
      <q-card-section class="bg-red text-white">
        <div class="text-h6">Cinelli</div>
        <div class="text-subtitle2">by cino cinelli</div>
      </q-card-section>

      <q-separator />

      <q-card-actions align="right">
        <q-btn flat>go to store</q-btn>
        <q-btn flat>smiliar bike</q-btn>
      </q-card-actions>
    </q-card>

    <q-card class="my-card">
      <q-card-section class="bg-purple text-white">
        <div class="text-h6">LOOK</div>
        <div class="text-subtitle2">by jean beyl</div>
      </q-card-section>

      <q-card-actions align="around">
        <q-btn flat>go to store</q-btn>
        <q-btn flat>smiliar bike</q-btn>
      </q-card-actions>
    </q-card>

    <q-card class="my-card">
      <q-card-section class="bg-teal text-white">
        <div class="text-h6">Raleigh</div>
        <div class="text-subtitle2">frank bowden</div>
      </q-card-section>

      <q-card-actions vertical align="right">
        <q-btn flat>go to store</q-btn>
        <q-btn flat>smiliar bike2</q-btn>
      </q-card-actions>
    </q-card>

    <q-card class="my-card">
      <q-card-section class="bg-grey-8 text-white">
        <div class="text-h6">dosnoventa</div>
        <div class="text-subtitle2">by detroit</div>
      </q-card-section>

      <q-card-actions vertical align="center">
        <q-btn flat>official web</q-btn>
        <q-btn flat>smiliar bike</q-btn>
      </q-card-actions>
    </q-card>
  </div>
    </q-drawer>

    <q-page-container>
      <div class="q-pa-md">
        <q-carousel
          swipeable
          animated
          arrows
          v-model="slide"
          v-model:fullscreen="fullscreen"
          infinite
        >
          <q-carousel-slide :name="1" img-src="https://i.ytimg.com/vi/7vXsE4e-PpM/maxresdefault.jpg" />
          <q-carousel-slide :name="2" img-src="https://bikerumor.com/wp-content/uploads/2020/10/2021-Look-795-Blade-RS-aero-road_300g-lighter-aerodynamic-carbon-road-race-bike_rainbow.jpg" />
          <q-carousel-slide :name="3" img-src="https://dosnoventabikes.com/wp-content/uploads/2020/10/Dosnoventa_DET_BLACK_Bike__Ride_2021.jpg" />
          <q-carousel-slide :name="4" img-src="https://i.pinimg.com/originals/01/17/1b/01171bc26173fe9188ea7272cd13dc49.jpg" />

          <template v-slot:control>
            <q-carousel-control
              position="bottom-right"
              :offset="[18, 18]"
            >
              <q-btn
                push round dense color="white" text-color="primary"
                :icon="fullscreen ? 'fullscreen_exit' : 'fullscreen'"
                @click="fullscreen = !fullscreen"
              />
            </q-carousel-control>
          </template>
        </q-carousel>
      </div>
    </q-page-container>
    <hr>

    <q-footer elevated class="bg-grey-8 text-white">
      <q-toolbar>
        <q-toolbar-title>
          <q-avatar>
            <img src="https://cdn.quasar.dev/logo-v2/svg/logo-mono-white.svg">
          </q-avatar>
          <div>DUnc</div>
        </q-toolbar-title>
      </q-toolbar>
    </q-footer>
  </q-layout>
</template>

<script>
import { ref } from 'vue'

export default {
  setup() {
    const leftDrawerOpen = ref(false)
    const rightDrawerOpen = ref(false)
    const slide = ref(1)
    const fullscreen = ref(false)

    function toggleLeftDrawer() {
      leftDrawerOpen.value = !leftDrawerOpen.value
    }

    function toggleRightDrawer() {
      rightDrawerOpen.value = !rightDrawerOpen.value
    }

    return {
      leftDrawerOpen,
      rightDrawerOpen,
      slide,
      fullscreen,
      toggleLeftDrawer,
      toggleRightDrawer
    }
  }
}
</script>
