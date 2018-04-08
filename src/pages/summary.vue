<template>
  <q-page padding>
    <h3 class="caption">Summary</h3>
    <p>Date of accident: {{ this.$store.state.date.dateOfAccident }} </p>
    <p>Age: {{ this.$store.state.profile.age }} </p>
    <p>Gender: {{ this.$store.state.profile.gender }} </p>
    <p>Ability to socialize after accident: {{this.$store.state.data.lossOfSociety}}</p>
    <p>Pre-accident monthly income: i{{ this.$store.state.profile.preAccidentIncome }} </p>
    <p>Expected retirement age: {{ this.$store.state.profile.ageOfRetirement }}  </p>
    <p>Incurred medical expenses {{ this.$store.state.profile.expenses }} </p>
    <p>Medical Report Received? {{this.$store.state.data.medicalReportExist}}</p>
    <div v-if="medicalReportExist">
      <p class="caption">Estimated loss of earning capacity: {{this.$store.state.data.earningCapacity}}</p>
    </div>
    <q-btn @click="$router.push('result')" color="white" text-color="black" label="Result" />
  </q-page>
</template>

<script>
export default {
  // name: 'PageName',
}
</script>

<style>
</style>
