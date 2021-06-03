<template>
    <div class="col-xs-12 col-sm-6">
        <ul class="list-group">
            <li class="list-group-item"
                v-for="index in 5"
                :key="index">

                Person #{{ index }}
                <button style="float:right;" @click="editPerson(index)">Edit</button>

            </li>
        </ul>
    </div>
</template>

<script>
    export default {
        methods: {
            editPerson(index) {
                alert("Editing Person #" + index);
            }
        }
    }
</script>

<style>

</style>
