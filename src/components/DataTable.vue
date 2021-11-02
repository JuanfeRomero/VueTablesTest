<template>
    <v-card>
        <v-card-title>
            Items Data
            <v-spacer/>
            <v-text-field
                v-model="search"
                append-icon="mdi-magnify"
                label="Search"
                single-line
                hide-details
            />
        </v-card-title>
        <v-data-table dark
            :headers="headers"
            :items="items"
            :search="search"
            :items-per-page="7"
            class="elevation-1"
        />
    </v-card>
</template>

<script>
export default {
    data(){
        return{
            search:'',
            headers:[
                {
                    text: 'Items in table',
                    align: 'start',
                    sortable: false,
                    value: 'name',
                },
                {text: 'Details', value:"details"}
        ],
            items: [
                {
                    name: "item 1",
                    details: "details 1"
                },
                {
                    name: "item 2",
                    details: "details 2"
                },
                {
                    name: "item 3",
                    details: "details 3"
                },
                {
                    name: "item 4",
                    details: "details 4"
                },
                {
                    name: "item 5",
                    details: "details 5"
                },
                {
                    name: "OOOOOTEM",
                    details: "OOOOOOOTAils"
                },
                {
                    name: "ZZZZZZMMMDFEFE",
                    details: "FRIJGJEINDOWNEFEG"
                },
                {
                    name: "Mario",
                    details: "Luigi"
                },
            ]
        }
    }

}
</script>