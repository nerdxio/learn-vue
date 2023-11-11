<script setup>
import { ref, onMounted } from 'vue'
import EventService from '../services/EventService'

const props = defineProps({
  id: {
    required: true,
  },
})

const event = ref(null)

onMounted(() => {
  EventService.getEvent(props.id)
    .then((response) => (event.value = response.data))
    .catch((error) => console.log(error))
})
</script>

<template>
  <div v-if="event">
    <h1>{{ event.title }}</h1>
    <p>{{ event.title }} on {{ event.data }} @ {{ event.location }}</p>
    <p>{{ event.description }}</p>
  </div>
</template>
