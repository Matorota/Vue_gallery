<template>

  <div class="block galleryBlock">
    
    <v-container>
      <h2 class="text-center">Vue Gallery</h2>
      <v-row>
        <v-col v-for="item in items" :key="item.id" class="d-flex child-flex" cols="2" sm="6">
          <v-card flat tile class="d-flex">
            <v-img :src="item.src" aspect-ratio="1" class="grey lighten-2">
              <template v-slot:placeholder>
                <v-row class="fill-height ma-0" align="center" justify="center">
                  <v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular>
                </v-row>
              </template>
            </v-img>
          </v-card>
        </v-col>
      </v-row>
          <div id="pagetop" class="fixed right-0 bottom-0" v-show="scY > 300" @click="toTop">
      <svg  width="48" height="48" viewBox="0 0 24 24" fill="none"
           stroke="#4a5568"
           stroke-width="1" stroke-linecap="square" stroke-linejoin="arcs">
        <path d="M18 15l-6-6-6 6"/>
      </svg>
    </div>
    </v-container>
  </div>
</template>

<script>
export default {
  name: "Gallery",
  data() {
    return {
      
      items: [
        {
          id: 1,
          src: require("../assets/images/img1.jpg")
        },
        {
          id: 2,
          src: require("../assets/images/img2.jpg")
        },
        {
          id: 3,
          src: require("../assets/images/img3.jpg")
        },
        {
          id: 4,
          src: require("../assets/images/img4.jpg")
        },
        {
          id: 5,
          src: require("../assets/images/img5.jpg")
        },
        {
          id: 6,
          src: require("../assets/images/img6.jpg")
        },
        {
          id: 7,
          src: require("../assets/images/img7.jpg")
        },
        {
          id: 8,
          src: require("../assets/images/img8.jpg")
        },
        
        {
          id: 9,
          src: require("../assets/images/img9.jpg")
        },
        {
          id: 10,
          src: require("../assets/images/img10.jpg")
        },
        {
          id: 11,
          src: require("../assets/images/img11.jpg")
        },
        {
          id: 12,
          src: require("../assets/images/img12.jpg")
        },
        {
          id: 13,
          src: require("../assets/images/img13.jpg")
        },
        {
          id: 14,
          src: require("../assets/images/img14.jpg")
        },
        {
          id: 15,
          src: require("../assets/images/img15.jpg")
        },
        {
          id: 16,
          src: require("../assets/images/img16.jpg")
        },
        {
          id: 17,
          src: require("../assets/images/img17.jpg")
        },
        {
          id: 18,
          src: require("../assets/images/img18.jpg")
        },
        {
          id: 19,
          src: require("../assets/images/img19.jpg")
        },
        {
          id: 20,
          src: require("../assets/images/img20.jpg")
        }
      ]
    };
  }
  
};
</script>