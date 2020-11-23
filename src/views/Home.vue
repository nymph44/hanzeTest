<template>
  <b-container>
    <b-row align-v="center">
      <Opleiding-kaart v-for="opleiding in opleidingen" :key="opleiding.id" :name="opleiding.name" :tijd="opleiding.tijd"></Opleiding-kaart>
   
    </b-row>
</b-container>
</template>

<script>
// @ is an alias to /src
import Card from '@/components/Card.vue';

export default {
  name: "Home",
  components: {"Opleiding-kaart": Card },
  mounted(){
    this.fetchData();
  },
  data(){
    return {
      opleidingen:[]
    }
  },
  methods: {
    async fetchData(){
      const res = await fetch("opleidingen.json");
      const val = await res.json();
      this.opleidingen = val;
      // console.log(val);
    }
  }
};
</script>
