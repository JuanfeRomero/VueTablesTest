<template>
  <v-simple-table dark fixed-header height="400px">
      <template v-slot:default>
          <thead>
              <tr>
                  <th class="text-left">Name</th>
                  <th class="text-left">Details</th>
              </tr>
          </thead>
          <tbody>
              <tr v-for="item in items" :key="item.key">
                  <td>{{ item.name }}</td>
                  <td>{{ item.details }}</td>
              </tr>
          </tbody>
      </template>
  </v-simple-table>
</template>

<script>
export default {
    data(){
        return{
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
            ]
        }
    }

}
</script>