<template>
    <div class="col-xs-12 col-sm-6">
        <p>Person Details will be shown here!</p>
        <p>Name: {{ details.firstName + " " + details.lastName }}</p>
        <p>Birthday: {{ details.birthday }}</p>
        <p>Blood Type: {{ details.bloodType }}</p>
    </div>
</template>

<script>
    export default {
        props: ['details']
    }
</script>

<style>

</style>
