<script setup lang="ts">
import {ref} from "vue";
import DatePicker from '@lib/date-time-picker/Vue3PersianDatetimePicker.vue'

const date = ref('');
const time = ref('');
</script>

<template>
  <div>
    <div>
      <date-picker v-model="date" />
      {{ date }}
    </div>

    <div style="margin-top:30px">
      <date-picker v-model="time" type="time" />
      {{ time }}
    </div>
  </div>
</template>

<style scoped lang="scss">
</style>
