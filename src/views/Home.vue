<template>
  <div class="home">
    <h1>💉 vaksine-kalkulatoren</h1>

    <p>Når tok du siste vaksinedose? <br/> </p>
      <p><i>(trykk på boksen under for å velge dato)</i></p>
    <input type="date" v-model="selected_date" />

    <div v-if="selected_date != 0">
      <p>Fulle uker siden du tok siste vaksinedose: <br/>
      <span class="big">{{ weeks }}</span></p>
    </div>

  </div>
</template>

<script>
  export default {
    name: "Home",

    data () {
      return {
        selected_date: 0
      }
    },

    computed: {
      weeks () {
        const ms_since = new Date () - new Date(this.selected_date) // millisekunder siden sist dose
        const weeks_since = ms_since / 604800000 // millisekunder per uke
        return Math.floor(weeks_since) // runder nedover for fulle uker
      }
    }
  };
</script>