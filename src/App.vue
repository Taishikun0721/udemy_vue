<template>
<div>
  <h2>{{ eventData.maxNumber }}</h2>
  <input type="text" v-model.lazy.number="eventData.maxNumber">
  <button @click="incrementNumber">増やす</button>
  <h2>{{ eventData.title }}</h2>
  <input type="text" v-model="eventData.title">
  <pre>{{ eventData.host }}</pre>
  <input type="text" v-model.trim="eventData.host">
  <label for="detail">イベントの内容</label>
  <pre>{{ eventData.detail }}</pre>
  <textarea id="detail" cols="30" rows="10" v-model="eventData.detail"></textarea>
  <input type="checkbox" id="isPrivate" v-model="eventData.isPrivate">
  <h2>{{ eventData.isPrivate }}</h2>
  <h2>参加条件</h2>
  <input type="checkbox" id="10" value="10代" v-model="eventData.target">
  <label for="10">10代</label>
  <input type="checkbox" id="20" value="20代" v-model="eventData.target">
  <label for="20">20代</label>
  <input type="checkbox" id="30" value="30代" v-model="eventData.target">
  <label for="30">30代</label>
  <h1>{{ eventData.target }}</h1>
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
export default {
  data() {
    return {
      locations: ['東京', '大阪', '福岡'],
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
  methods: {
    incrementNumber() {
      this.eventData.maxNumber += 1
    }
  }
}
</script>
