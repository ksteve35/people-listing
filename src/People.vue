<template>
    <div class="col-xs-12 col-sm-6">
        <ul class="list-group">
            <li class="list-group-item"
                v-for="index in 5"
                :key="index">

                Person #{{ index }}
                <button style="float:right;" @click="getPersonDetails(index)">Details</button>
                <button style="float:right;" @click="editPerson(index)">Edit</button>

            </li>
        </ul>
    </div>
</template>

<script>
    export default {
        props: [

        ],
        methods: {
            editPerson(index) {
                console.log("Editing Person #" + index);
            },
            getPersonDetails(index) {
                console.log("Getting Person #" + index);
            }
        }
    }
</script>

<style>

</style>
