<script setup>
import EventCard from '@/components/EventCard.vue'
import { ref } from 'vue'

const events = ref([
  {
    id: 1,
    category: 'music',
    title: 'Event 1',
    description: 'This is the first event',
    location: 'London, UK',
    date: 'Jan 1, 2022',
    time: '15:00',
    petsAllowed: true,
    organizer: 'John Doe',
  },
  {
    id: 2,
    category: 'food',
    title: 'Event 2',
    description: 'This is the second event',
    location: 'New York, USA',
    date: 'Feb 2, 2022',
    time: '16:00',
    petsAllowed: false,
    organizer: 'Jane Doe',
  },
  {
    id: 3,
    category: 'drinks',
    title: 'Event 3',
    description: 'This is the third event',
    location: 'Paris, FR',
    date: 'Mar 3, 2022',
    time: '17:00',
    petsAllowed: true,
    organizer: 'John Smith',
  },
  {
    id: 4,
    category: 'other',
    title: 'Event 4',
    description: 'This is the fourth event',
    location: 'Sydney, AU',
    date: 'Apr 4, 2022',
    time: '18:00',
    petsAllowed: false,
    organizer: 'Jane Smith',
  },
  {
    id: 5,
    category: 'music',
    title: 'Event 5',
    description: 'This is the fifth event',
    location: 'Tokyo, JP',
    date: 'May 5, 2022',
    time: '19:00',
    petsAllowed: true,
    organizer: 'John Doe',
  },
  {
    id: 6,
    category: 'food',
    title: 'Event 6',
    description: 'This is the sixth event',
    location: 'Rio de Janeiro, BR',
    date: 'Jun 6, 2022',
    time: '20:00',
    petsAllowed: false,
    organizer: 'Jane Doe',
  },
  {
    id: 7,
    category: 'drinks',
    title: 'Event 7',
    description: 'This is the seventh event',
    location: 'Berlin, DE',
    date: 'Jul 7, 2022',
    time: '21:00',
    petsAllowed: true,
    organizer: 'John Smith',
  },
])
</script>

<template>
  <h1>Events For Good</h1>
  <div class="events">
    <EventCard v-for="event in events" :key="event.id" :event="event" />
  </div>
</template>

<style scoped>
.events {
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>
