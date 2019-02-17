<script>
export default {
  name: 'EventCard',
  props: {
    customer: {
      type: 'String',
      default: ''
    },
    resource: {
      type: 'String',
      default: ''
    },
    image: {
      type: 'String',
      default: ''
    }
  },
  data() {
    return {
      cardHeight: 250
    }
  }
}
</script>
