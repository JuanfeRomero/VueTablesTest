<template>
    <v-container fluid>
        <v-data-iterator
            :items="lists"
            item-key="name"
            :items-per-page="4"
            :single-expand="true"
            hide-default-footer
        >
            <template v-slot:default="{ items, isExpanded, expand}">
                <v-row>
                    <v-col
                        v-for="item in items"
                        :key="item.name"
                        cols="12"
                        sm="6"
                        md="4"
                        lg="3"
                    >
                        <v-card>
                            <v-card-title>
                                <h4>{{ item.name }}</h4>
                            </v-card-title>
                            <v-switch
                                :input-value="isExpanded(item)"
                                :label="isExpanded(item) ? 'Expanded' : 'Closed'"
                                class="pl-4 mt-0"
                                @change="(v) => expand(item, v)"
                            />
                            <v-divider/>
                            <v-list
                                v-if="isExpanded(item)"
                                dense
                            >
                                <v-list-item
                                    v-for="(it, i) in item.content"
                                    :key="i"
                                >
                                    <v-list-item-content>{{it}}</v-list-item-content>
                                </v-list-item>
                            </v-list>
                        </v-card>
                    </v-col>
                </v-row>
            </template>
        </v-data-iterator>
    </v-container>
</template>

<script>
export default {
    data: () =>({
        lists: [
            {
                name: "Flowers",
                content: ["Passion Flower", "Poppy", "Hybrid Tea Roses", "Hosta", "Catmint", "Morning Glory", "Narcissus", "Rhododendron", "Camelia", "Cyclamen", "Petunias", "Cosmos"]
            },
            {
                name: "Vacations",
                content: ["Madrid", "Philadelphia", "San Antonio, Texas", "Cairo", "Rio de Janeiro", "San Diego", "Montreal", "Sesame Place", "British Virgin Islands", "San Francisco", "Virginia Beach", "Dubai"]
            },
            {
                name: "Movies",
                content: ["Luca", "Sinkhole", "Madres", "The Forgotten Battle", "Teen Titans Go!", "Avengers", "Carriers", "Naruto the movie", "Malignant", "Night Teeth", "Gunpowder Milkshake", "Bartkowiak"]
            },
            {
                name: "Corporate Cliches",
                content: ["Let's get granular",
                "Boots on the ground",
                "Hit the ground running", 
                "Don't throw out the baby with the bathwater", 
                "At the end of the day", 
                "Low-hanging fruit",
                "Resonate",
                "The reward for good work is more work",
                "The 80/20 rule",
                "Run it up the flagpole",
                "Crunch time",
                "Manage Expectations"],
            },
        ]
    })
}
</script>

<style>

</style>