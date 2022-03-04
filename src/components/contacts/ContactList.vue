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
    items: [
      {
        id: 1,
        name: "bolo",
        email: "bollo@gmial.com",
        phone: 545234324,
        isFavorite: false,
      },
      {
        id: 2,
        name: "bollo",
        email: "bollo@gmial.com",
        phone: 5451234324,
        isFavorite: false,
      },
      {
        id: 3,
        name: "bo",
        email: "bollo@gmial.com",
        phone: 545233234,
        isFavorite: false,
      },
      {
        id: 4,
        name: "Gordolobo",
        email: "bollo@gmial.com",
        phone: 2345234324,
        isFavorite: false,
      },
      {
        id: 5,
        name: "bolasdo",
        email: "bollo@gmial.com",
        phone: 145234324,
        isFavorite: false,
      },
      {
        id: 6,
        name: "bolas",
        email: "bollo@gmial.com",
        phone: 125234324,
        isFavorite: false,
      },
    ],
  }),
};
</script>