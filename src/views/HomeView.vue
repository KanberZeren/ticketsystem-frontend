<template>
  <div id="app">
    <div class="home">
      <router-view></router-view>
      <HomePage msg="Welcome to our Ticketsystem!"/>
      <TicketListe/>
      <FooterBar/>
    </div>
  </div>
</template>

<script>
import HomePage from '@/components/HomePage.vue'
import TicketListe from '@/components/TicketListe.vue'
import FooterBar from '@/components/FooterBar.vue'

export default {
  name: 'HomeView',
  components: {
    FooterBar,
    HomePage,
    TicketListe
  }
}
</script>

<style scoped>
HomePage{
  margin-left: 20px;
  flex-direction: column;
  padding: 20px;
}
</style>
