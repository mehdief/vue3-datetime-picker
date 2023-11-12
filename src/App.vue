<script setup lang="ts">
import {ref} from "vue";
import DatePicker from '@lib/date-time-picker/Vue3PersianDatetimePicker.vue'

const tom = new Date();
tom.setDate(13);

const date = ref(tom);
const time = ref();
</script>

<template>
  <div>
    <div>
      <input type="text" id="date-picker-input">
      <date-picker v-model="date" format="date" custom-input_="#date-picker-input">
      </date-picker>
      <br>
      {{ date ?? 'null' }}
      <br>
      <button type="button" @click="date = new Date()">Set</button>
    </div>

    <div style="margin-top:30px">
      <date-picker v-model="time" type="time">
      </date-picker>
      {{ time }}
    </div>
  </div>
</template>
