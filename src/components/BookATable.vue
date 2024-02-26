<template>
  <div>
    <h1>Book a Table</h1>
    <div class="container">
    <form @submit.prevent="bookTable">
      <label for="name">Name:</label>
      <input type="text" id="name" v-model="name" required />

      <label for="email">Email:</label>
      <input type="email" id="email" v-model="email" required />

      <label for="date">Date:</label>
      <input type="date" id="date" v-model="date" required />

      <label for="time">Time:</label>
      <input type="time" id="time" v-model="time" required />

      <label for="guests">Number of Guests:</label>
      <input type="number" id="guests" v-model="guests" min="1" required />

      <button type="submit">Book Table</button>
    </form>
  </div>
  </div>
</template>

<style scoped>
.container{
  width: 100px;
  height:100%;
}
</style>

<script setup>
import { name, email, date, time, guests, bookTable, reset } from '../stores/Booking';
</script>
