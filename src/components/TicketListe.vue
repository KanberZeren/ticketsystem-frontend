<template>
  <div>
    <h1>Alle Tickets</h1>
    <ul>
      <li v-for="ticket in tickets" :key="ticket.id">
        {{ ticket.ticketNummer}} - {{ ticket.betreff }} - Status: {{ ticket.status }}
      </li>
    </ul>
  </div>
</template>

<script>
import axios from 'axios'

export default {
  name: 'TicketListe',
  data () {
    return {
      tickets: []
    }
  },
  mounted () {
    this.fetchTickets()
  },
  methods: {
    fetchTickets () {
      axios.get('http://localhost:8080/tickets')
        .then(response => {
          this.tickets = response.data
        })
        .catch(error => {
          console.error('Fehler beim Abrufen der Tickets', error)
        })
    }
  }
}
</script>

<style>
</style>
