<template>
  <div class="container">
    <app-header></app-header> 
    <hr>
    <div class="row">
      <app-people :people="people"></app-people>
      <app-person-details></app-person-details>
    </div>
  </div>
</template>

<script>
    import Header from './Header.vue';
    import People from './People.vue';
    import PersonDetails from './PersonDetails.vue';

    export default {
      data() {
        return {
          people: [{
            firstName: "Kyle",
            lastName: "Stevenson",
            birthday: "2/25/1997",
            bloodType: "B-"
          },
          {
            firstName: "Joe",
            lastName: "Smith",
            birthday: "6/29/1995",
            bloodType: "AB+"
          },
          {
            firstName: "Jane",
            lastName: "Doe",
            birthday: "11/14/1999",
            bloodType: "A+"
          },
          {
            firstName: "Bill",
            lastName: "Gates",
            birthday: "10/28/1955",
            bloodType: "B+"
          },
          {
            firstName: "Steve",
            lastName: "Jobs",
            birthday: "2/24/1955",
            bloodType: "O-"
          }]
        };
      },
      components: {
          'app-header': Header,
          'app-people': People,
          'app-person-details': PersonDetails
      }
    }
</script>

<style>

</style>
