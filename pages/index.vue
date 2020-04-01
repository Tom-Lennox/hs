<template>
  <v-layout wrap>
    <!-- <v-layout column justify-center align-center> -->
    <!-- ■carousel -->
    <v-carousel>
      <!-- cycle：ループ -->
      <!-- gradient: 何か重要なお知らせ等を表示したり。 -->
      <v-carousel-item
        v-for="item in items"
        :key="item"
        cycle="true"
        touch="left"
        :src="item.src"
        :gradient="item.gradient"
        :href="item.link"
        ><v-sheet height="100%" style="background-color: transparent;">
          <v-row class="fill-height" align="center" justify="center">
            <div class="display-3">{{ item.alertMessage }}</div>
          </v-row>
        </v-sheet>
        <!-- <v-sheet :color="color" height="100%" tile>
          <v-row classs="fill-height" align="center" justify="center">
            <div class="display-3">slide: {{ i + 1 }}</div>
          </v-row>
        </v-sheet> -->
      </v-carousel-item>
    </v-carousel>
    <!--  -->
    <!-- ■card -->
    <!-- 画像 -->
    <!-- <v-container grid-list-lg> ：箱状のものに詰めることができる。 -->
    <v-container grid-list-lg>
      <v-layout row wrap class="meal-plans">
        <v-flex v-for="photo in photos" :key="photo" xs4 sm4 md4
          ><v-card outlined raised :href="photo.link">
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
                      <span class="headline white--text">hoge</span>
                    </v-flex>
                  </v-layout>
                </v-container>
              </v-img>
            </v-responsive>
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
    <!-- <v-flex xs12 sm8 md6>
      <div class="text-center">
        <logo />
        <vuetify-logo />
      </div>
      <v-card>
        <v-card-title class="headline">
          Welcome to the Vuetify + Nuxt.js template
        </v-card-title>
        <v-card-text>
          <p>
            Vuetify is a progressive Material Design component framework for
            Vue.js. It was designed to empower developers to create amazing
            applications.
          </p>
          <p>
            For more information on Vuetify, check out the
            <a href="https://vuetifyjs.com" target="_blank"> documentation </a>.
          </p>
          <p>
            If you have questions, please join the official
            <a href="https://chat.vuetifyjs.com/" target="_blank" title="chat">
              discord </a
            >.
          </p>
          <p>
            Find a bug? Report it on the github
            <a
              href="https://github.com/vuetifyjs/vuetify/issues"
              target="_blank"
              title="contribute"
            >
              issue board </a
            >.
          </p>
          <p>
            Thank you for developing with Vuetify and I look forward to bringing
            more exciting features in the future.
          </p>
          <div class="text-xs-right">
            <em><small>&mdash; John Leider</small></em>
          </div>
          <hr class="my-3" />
          <a href="https://nuxtjs.org/" target="_blank">
            Nuxt Documentation
          </a>
          <br />
          <a href="https://github.com/nuxt/nuxt.js" target="_blank">
            Nuxt GitHub
          </a>
        </v-card-text>
        <v-card-actions>
          <v-spacer />
          <v-btn color="primary" nuxt to="/inspire">
            Continue
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-flex> -->
  </v-layout>
</template>

<script>
// import Logo from '~/components/Logo.vue'
// import VuetifyLogo from '~/components/VuetifyLogo.vue'

export default {
  components: {
    // Logo,
    // VuetifyLogo
  },
  data: () => ({
    // colors: ['primary', 'secondary', 'yellow darken-2', 'red', 'orange'],
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
