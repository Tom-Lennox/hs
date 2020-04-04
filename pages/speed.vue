<template>
  <v-layout wrap>
    <!-- <v-layout column justify-center align-center> -->
    <!-- ■card -->
    <!-- 画像 -->
    <!-- <v-container grid-list-lg> ：箱状のものに詰めることができる。 -->
    <v-container grid-list-lg>
      <v-layout row wrap class="meal-plans">
        <v-flex v-for="photo in photos" :key="photo" xs4 sm4 md4
          ><v-card raised :href="photo.link" :color="MenuCardColor">
            <!-- <v-card-title class="headline">
            {{ photo.title }}
          </v-card-title>
          <v-card-text>
            {{ photo.text }}
          </v-card-text> -->
            <v-responsive>
              <v-img
                src="https://cdn.pixabay.com/photo/2015/12/08/00/26/food-1081707_1280.jpg"
                height="200px"
              >
                <v-container fill-height fluid>
                  <v-layout fill-height>
                    <v-flex xs12 align-end flexbox>
                      <!-- <span class="headline white--text">hoge</span> -->
                    </v-flex>
                  </v-layout>
                </v-container>
              </v-img>
            </v-responsive>
            <!-- <div>入れちゃう。 -->
            <v-card-text
              ><h3>title</h3>
              <div>
                aaa
              </div></v-card-text
            >
          </v-card>
        </v-flex>
      </v-layout>
    </v-container>
    <!--  -->
    <!-- ■card -->
    <v-flex
      v-for="info in infos"
      :key="info"
      class="text-center"
      xs12
      sm12
      md12
      lg12
      xl12
      text-center
      my-1
      ><v-card max-width="1200" class="mx-auto"
        ><v-card-title class="headline">
          {{ info.title }}
        </v-card-title>
        <v-card-text>
          {{ info.text }}
        </v-card-text>
      </v-card>
    </v-flex>
    <!--  -->
  </v-layout>
</template>

<script>
export default {
  components: {
    // Logo,
    // VuetifyLogo
  },
  data: () => ({
    MenuCardColor: 'rgba(208, 147, 82, 0.4)',
    items: [
      {
        src:
          'https://cdn.pixabay.com/photo/2015/12/08/00/26/food-1081707_1280.jpg',
        gradient: 'to top right, rgba(0,0,0,.5), rgba(0,0,0,.8)',
        link:
          'https://cdn.pixabay.com/photo/2015/12/08/00/26/food-1081707_1280.jpg',
        alertMessage: '- Sold Out -'
      },
      {
        src:
          'https://cdn.pixabay.com/photo/2015/12/08/00/26/food-1081707_1280.jpg',
        gradient: '',
        link:
          'https://cdn.pixabay.com/photo/2015/12/08/00/26/food-1081707_1280.jpg',
        alertMessage: ''
      },
      {
        src:
          'https://cdn.pixabay.com/photo/2015/12/08/00/26/food-1081707_1280.jpg',
        gradient: '',
        link:
          'https://cdn.pixabay.com/photo/2015/12/08/00/26/food-1081707_1280.jpg',
        alertMessage: ''
      }
    ],
    infos: [
      {
        title: '重要なお知らせ',
        text: 'text'
      },
      {
        title: 'お知らせ',
        text: 'text'
      }
    ],
    photos: [
      {
        title: 'http',
        link:
          'https://cdn.pixabay.com/photo/2015/12/08/00/26/food-1081707_1280.jpg'
      },
      {
        title: 'http',
        link:
          'https://cdn.pixabay.com/photo/2015/12/08/00/26/food-1081707_1280.jpg'
      },
      {
        title: 'http',
        link:
          'https://cdn.pixabay.com/photo/2015/12/08/00/26/food-1081707_1280.jpg'
      },
      {
        title: 'http',
        link:
          'https://cdn.pixabay.com/photo/2015/12/08/00/26/food-1081707_1280.jpg'
      },
      {
        title: 'http',
        link:
          'https://cdn.pixabay.com/photo/2015/12/08/00/26/food-1081707_1280.jpg'
      }
    ]
  })
}
</script>
