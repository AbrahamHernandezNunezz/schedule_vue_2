<template>
<div>
<h2>CONTACTOS:</h2>
  <v-data-table
    :headers="headers"
    :items="items"
    :items-per-page="5"
    class="elevation-1"
  ></v-data-table>
</div>
</template>

<script>
export default {
  name: "ContactList",
  data: () => ({
    headers: [
      { align: "center",text: "Name", value: "name" },
      { text: "Email", value: "email" },
      { text: "Phone", value: "phone" },
      { text: "Favorite", value: "isFavorite" }
    ],
  }),
  props: ["items"]
};
</script>