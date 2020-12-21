<template>
<div>
  <LikeHeader :headerText="hello">>
    <template v-slot:test>
      <h2>testSlot</h2>
    </template>
    <h1>I am default slot</h1>
  </LikeHeader>
  <LikeNumber :total-number="number" v-on:increment-click="incrementNumber"></LikeNumber>
  <LikeNumber :total-number="number" v-on:increment-click="incrementNumber"></LikeNumber>
  <LikeFooter></LikeFooter>
  <div>
    <h2>イベントのフォーム</h2>
    <label for="title"></label>
    <input type="text" id="title" v-model.lazy="eventData.title">
    <p>{{eventData.title}}</p>

     <h2>最大人数</h2>
    <label for="maxNumber"></label>
    <input type="number" id="maxNumber" v-model.number="eventData.maxNumber">
    <p>{{eventData.maxNumber}}</p>
  </div>


</div>

</template>

<script>
import LikeHeader from './components/LikeHeader.vue'
import LikeFooter from './components/LikeFooter.vue'
export default {
  data() {
    return {
      number: 1000,
      hello: "hello Vue.js",
      eventData: {
        title: 'タイトル',
        maxNumber: 100
      }
    };
  },
  components: {
    LikeHeader,
    LikeFooter
  },
  methods: {
    incrementNumber: function(value) {
      this.number = value
    }
  }
}
</script>

<style scoped>
</style>

