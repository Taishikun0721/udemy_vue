<template>
<div>
  <Home></Home>
  <LikeHeader :header-text="title"></LikeHeader>
  <LikeNumber :total-number="totalNumber" @increment-click="totalNumber = $event"></LikeNumber>
  <h2>{{ eventData.maxNumber }}</h2>
  <input type="text" v-model.lazy.number="eventData.maxNumber">
  <button @click="incrementNumber">増やす</button>
  <EventTitle v-model="eventData.title"></EventTitle>
  <EventHost v-model="eventData.host"></EventHost>
  <EventDetail v-model="eventData.detail"></EventDetail>
  <EventIsPrivate v-model="eventData.isPrivate"></EventIsPrivate>


  <input type="radio" id="free" value="無料" v-model="eventData.price">
  <label for="free"> 無料だよ</label>
  <input type="radio" id="payd" value="有料" v-model="eventData.price">
  <label for="payd"> 有料だよ</label>
  <select v-model="eventData.location">
    <option v-for="location in locations" :key="location">{{ location }}</option>
  </select>
  <h2>{{ eventData.location }}</h2>
</div>
</template>

<script>
import LikeHeader from './components/LikeHeader.vue'
import LikeNumber from './components/LikeNumber.vue'
import EventTitle from './components/EventTitle.vue'
import EventHost from './components/EventHost.vue'
import EventDetail from './components/EventDetail.vue'
import EventIsPrivate from './components/EventIsPrivete'
import Home from './components/Home.vue'
export default {
  data() {
    return {
      locations: ['東京', '大阪', '福岡'],
      title: "これはブログのタイトルです。",
      totalNumber: 1000,
      eventData: {
        maxNumber: 100,
        title: "This is a title",
        host: "",
        detail: "",
        isPrivate: false,
        target: [],
        price: "無料",
        locatios: '東京'
      }
    }
  },
  components: {
    EventTitle,
    EventHost,
    EventDetail,
    EventIsPrivate,
    LikeHeader,
    LikeNumber,
    Home,
  },
  methods: {
    incrementNumber() {
      this.eventData.maxNumber += 1
    }
  }
}
</script>
