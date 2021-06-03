<template>
  <div class="container">
    <app-header></app-header> 
    <hr>
    <div class="row">
      <app-people></app-people>
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
