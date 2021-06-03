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
        props: {
            people: [{
                firstName: { type: String},
                lastName: { type: String},
                birthday: { type: String},
                bloodType: { type: String}
            }]
        },
        methods: {
            editPerson(index) {
                console.log("Editing Person #" + index);
            },
            getPersonDetails(index) {
                console.log("Getting Person #" + index);
            },
            personDisplayName(index) {
                return this.people[index].lastName + ", " + this.people[index].firstName;
            }
        }
    }
</script>

<style>

</style>
