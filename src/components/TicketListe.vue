<template>
  <div>
    <h1 class="mb-4">Alle Tickets</h1>
    <table class="table table-bordered table-hover">
      <thead class="thead-dark">
      <tr>
        <th>ID</th>
        <th>Betreff</th>
        <th>Nachricht</th>
        <th>Status</th>
        <th>Erstellt am</th>
      </tr>
      </thead>
      <tbody>
      <tr v-for="ticket in tickets" :key="ticket.id">
        <td>{{ ticket.id }}</td>
        <td>{{ ticket.betreff }}</td>
        <td>{{ ticket.nachricht }}</td>
        <td>{{ ticket.status }}</td>
        <td>{{ formatDateTime(ticket.erstelltAm) }}</td>
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
    },
    formatDateTime (dateTimeString) {
      const options = { year: 'numeric', month: 'numeric', day: 'numeric', hour: 'numeric', minute: 'numeric', second: 'numeric' }
      const dateTime = new Date(dateTimeString)
      return dateTime.toLocaleDateString('de-DE', options)
    }
  }
}
</script>

<style>
</style>
