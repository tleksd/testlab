<template>
  <div>
    <p v-for="manu in manufacturer" :key="manu.id">
      {{ manu.id }} - {{ manu.Title }}
    </p>
    <input placeholder="id" v-model="id" />
    <input placeholder="Title" v-model="Title" />
    <buttom @click="post()">Post</buttom>
    <buttom @click="put()">Put</buttom>
    <buttom @click="remove()">Delete</buttom>
  </div>
</template>

<script>
import axios from "axios"

export default {
  data() {
    return {
      text: "test",
      manufacturer: [{ id: 1, Title: "test1"}]
    };
  },
  created() {

  },
  methods: {
    get(){
      axios.get("-----").then((respone)) =>
        this.manufacturer = respone.data;
      
    }
  }
};
</script>
