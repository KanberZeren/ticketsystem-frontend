<script>
import axios from 'axios'

export default {
  getAllTickets () {
    return axios.get('http://localhost:8080/tickets')
  }
}
</script>

<style scoped>
</style>
