<template>
  <div class="home">
    <HomePage msg="Welcome to our Ticketsystem!"/>
    <TicketListe/>
  </div>
</template>

<script>
import HomePage from '@/components/HomePage.vue'
import TicketListe from '@/components/TicketListe.vue'

export default {
  name: 'HomeView',
  components: {
    HomePage,
    TicketListe
  }
}
</script>

<style scoped>
.home {
  margin-left: 20px;
  margin-left: 20px;
  flex-direction: column;
  padding: 20px;
}
</style>
