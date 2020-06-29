<template>
  <v-container class="pa-4 text-center">
    <v-row class="fill-height" align="middle" justify="center">
      <template v-for="(item, i) in items">
        <v-col
          :key="i"
          cols="12"
          md="4"
        >
          <v-hover v-slot:default="{ hover }">
            <v-card
            class="mx-auto"
            color= "transparent"
            max-width="225"
            :elevation="hover ? 12 : 2"
            :class="{ 'on-hover': hover }"
            >
            <v-img :aspect-ratio="9/9" :src="item.img"></v-img>
            
            </v-card>
          </v-hover>
          <v-card-text
        class="pt-6"
        style="position: relative;"
      >
        <h3 class="display-1 font-weight-light light-blue--text mb-2">{{ item.title }}</h3>
        <div class="font-weight-light title mb-2"> {{ item.subtext }}<br>
          
        </div>
      </v-card-text>
        </v-col>
      </template>
    </v-row>
  </v-container>
</template>

<script>
  export default {
    data: () => ({
      items: [
        {
            title: 'Playing Basketball',
            subtext: 'I’ve been playing for over 10 years and have been apart of various different teams throughout the years.I find that it is great way of being social while being able to workout.',
            img: 'https://www.pngitem.com/pimgs/m/3-32259_png-basketball-black-and-white-basketball-icon-png.png',
        },
        {
            title: 'Listening to Music',
            subtext:'Recently I’ve been binging on Hip-Hop and R&B classics as well as finding and listening to new up and coming artists.',
            img: 'https://png.pngtree.com/png-vector/20190605/ourlarge/pngtree-headphones-icon-png-image_1477434.jpg'
        },
        {
            title: 'Investing',
            subtext:'I also enjoy researching and learning how to invest in the stock market to reach my long term financial goals. ',
          img: 'https://cdn0.iconfinder.com/data/icons/stock-investment-2/66/29-512.png',
        },
      ],
      transparent: 'rgba(255, 255, 255, 0)',
    }),
  }
</script>

<style scoped>
.v-card {
  transition: opacity .4s ease-in-out;
}

.v-card:not(.on-hover) {
  opacity: 0.6;
 }

</style>