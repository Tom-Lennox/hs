<template>
  <v-layout>
    <v-flex class="text-center">
      <!-- ■breadcrumb -->
      <div>
        <v-breadcrumbs :items="items" divider=">"></v-breadcrumbs>
      </div>
      <!--  -->
      <v-img
        src="https://cdn.pixabay.com/photo/2015/12/08/00/26/food-1081707_1280.jpg"
        gradient="to top right, rgba(0,0,0,.5), rgba(0,0,0,.8)"
      ></v-img>
      <!-- ■card -->
      <!-- 通常はコンポーネント呼び出ししそう。 -->
      <v-layout wrap>
        <v-flex
          v-for="info in infos"
          :key="info"
          xs12
          sm12
          md4
          text-center
          my-5
        >
          <v-card min-width="500" class="mx-auto">
            <v-card-title>title{{ info.title }}</v-card-title>
            <v-card-text>contents{{ info.descriptions }}.</v-card-text>
            <v-card-actions>
              <!-- ここでv-btn textはUI悪い。 -->
              <!-- <v-btn text>more{{ n }}</v-btn> -->
            </v-card-actions>
          </v-card>
        </v-flex>
      </v-layout>
      <!--  -->
      <!--  -->
      <!-- ■expansions -->
      <!-- これもコンポーネントで使用しそう。 -->
      <v-expansion-panels>
        <v-expansion-panel v-for="(item, i) in 5" :key="i">
          <v-expansion-panel-header>- expansion -</v-expansion-panel-header>
          <v-expansion-panel-content
            >content. brbrbrbrbrbrbrbrbrbr</v-expansion-panel-content
          >
        </v-expansion-panel>
      </v-expansion-panels>
      <!--  -->
      <!-- ■calender -->
      <calender />
      <!--  -->
    </v-flex>
  </v-layout>
</template>
<script>
import calender from './calener'

export default {
  components: {
    calender
  },
  data() {
    return {
      items: [
        {
          text: 'Home',
          disabled: false,
          href: 'http://yahoo.co.jp'
        },
        {
          text: 'food',
          disabled: false,
          href: '../menu.html'
        },
        {
          text: 'なんちゃらバーガー',
          disabled: true,
          href: '../hogeburger.html'
        }
      ],
      colors: ['primary', 'secondary', 'yellow darken-2', 'red', 'orange'],
      events: [
        {
          name: 'aaa',
          start: '2020-03-14',
          end: '2020-03-20'
        }
      ],
      infos: [
        {
          title: 'こだわり',
          description: '肉がなんたら'
        },
        {
          title: 'アレルゲン情報',
          description: '小麦粉、大豆'
        },
        {
          title: 'other',
          description: 'etc'
        }
      ]
    }
  }
}
</script>
