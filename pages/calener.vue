<template>
  <v-layout>
    <!-- ■calender -->
    <!-- <v-layout justify-center>
      <v-card-title class="font-weight-bold">2020/03 Business Day</v-card-title>
    </v-layout> -->
    <!-- margin：細かい指定は下記 -->
    <!-- https://vuetifyjs.com/ja/styles/spacing/ -->
    <!-- footerと重なるのでmb-10 -->
    <v-flex md-4 xs12 class="mb-10 mx-10">
      <!-- <v-card-title class="font-weight-bold"></v-card-title> -->
      <v-sheet height="500">
        <p>2020/03 Business Day</p>
        <v-calendar
          type="month"
          now="2020-03-16"
          value="2020-03-15"
          :events="events"
        ></v-calendar>
      </v-sheet>
    </v-flex>
  </v-layout>
</template>
<!--  -->
<script>
export default {
  data() {
    return {
      events: [
        {
          name: 'aaa',
          start: '2020-03-14',
          end: '2020-03-20'
        }
      ]
    }
  }
}
</script>
