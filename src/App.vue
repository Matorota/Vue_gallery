<template>
  <v-app> 

    <v-app-bar flat max-height="65">
      <Header /> 
      

    </v-app-bar>
    <div id="pagetop" class="fixed right-0 bottom-0" v-show="scY > 300" @click="toTop">
      <svg  width="48" height="48" viewBox="0 0 24 24" fill="none"
           stroke="#4a5568"
           stroke-width="1" stroke-linecap="square" stroke-linejoin="arcs">
        <path d="M18 15l-6-6-6 6"/>
      </svg>
      
    </div>
    
    <router-view > <!-- v-for="(galerija, i) in galerija_list" :key="i" :galerija="galerija"  -->


</router-view>
<Button /> 
  </v-app>
  
</template>

<script>

import Header from "./components/common/Header";
import Button from "./components/common/Button_top";
import GalleryVue from './components/Gallery.vue';

export default {
  name: "App",

  components: {
    Header,
    Button,
  },

  data() {
      return {
        scTimer: 0,
        scY: 0,
      }
    },
    methods: {
		getGallery() {
			// const photos = [

			// ];
			const galerija = [];
			for (let i = 0; i < 20; i++) {
        GalleryVue
			}
			return galerija;
		},
		handleScroll() {
			if (
				window.scrollY + window.innerHeight >=
				document.body.scrollHeight - 50
			) {
				const new_gallery = this.getGallery();
				this.galerija_list = [...this.galerija_list, ...new_gallery];
			}
		},
	},
	mounted() {
		this.anime_list = this.getGallery();
		window.addEventListener("scroll", this.handleScroll);
	},
};
</script>
