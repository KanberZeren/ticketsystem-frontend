<script>
import axios from 'axios'

export default {
  getAllTickets () {
    return axios.get('http://localhost:8080/tickets')
  },
  deleteTicket (ticketId) {
    return axios.delete(`http://localhost:8080/ticket/${ticketId}`)
  }
}
</script>

<style scoped>
</style>
