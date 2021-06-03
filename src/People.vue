<template>
    <div class="col-xs-12 col-sm-6">
        <ul class="list-group">
            <li class="list-group-item"
                v-for="(people, index) in people"
                :key="index">
                
                {{ personDisplayName(index) }}
                <button style="float:right;" @click="getPersonDetails(index)">Details</button>
                <button style="float:right;" @click="editPerson(index)">Edit</button>

            </li>
        </ul>
    </div>
</template>

<script>
    export default {
        props: ['people'],
        methods: {
            editPerson(index) {
                console.log("Editing " + this.people[index].firstName + " " + this.people[index].lastName + "\nFeature not yet implemented!");
            },
            getPersonDetails(index) {
                console.log("Getting " + this.people[index].firstName + " " + this.people[index].lastName);
                this.$emit('displayDetails', this.people[index]);
            },
            personDisplayName(index) {
                return this.people[index].lastName + ", " + this.people[index].firstName;
            }
        }
    }
</script>

<style>

</style>
