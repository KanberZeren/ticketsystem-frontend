<template>
  <div>
    <h1>Alle Tickets</h1>
    <table>
      <thead>
      <tr>
        <th>ID</th>
        <th>Betreff</th>
        <th>Nachricht</th>
        <!-- Add other columns as needed -->
      </tr>
      </thead>
      <tbody>
      <tr v-for="ticket in tickets" :key="ticket.id">
        <td>{{ ticket.id }}</td>
        <td>{{ ticket.betreff }}</td>
        <td>{{ ticket.nachricht }}</td>
      </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
import ticketService from '@/router/ticketService'

export default {
  data () {
    return {
      tickets: []
    }
  },
  created () {
    this.fetchTickets()
  },
  methods: {
    async fetchTickets () {
      try {
        const response = await ticketService.getAllTickets()
        this.tickets = response.data
      } catch (error) {
        console.error('Fehler beim Abrufen der Tickets:', error)
      }
    }
  }
}
</script>

<style>
</style>
