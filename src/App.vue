<template>
  <v-app>
    <v-app-bar app color="primary" dark>
      <div class="d-flex align-center">
        <v-img
          alt="Vuetify Logo"
          class="shrink mr-2"
          contain
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-logo-dark.png"
          transition="scale-transition"
          width="40"
        />

        <v-img
          alt="Vuetify Name"
          class="shrink mt-1 hidden-sm-and-down"
          contain
          min-width="100"
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-name-dark.png"
          width="100"
        />
      </div>

      <v-spacer></v-spacer>

      <v-btn
        href="https://github.com/vuetifyjs/vuetify/releases/latest"
        target="_blank"
        text
      >
        <span class="mr-2">Latest Release</span>
        <v-icon>mdi-open-in-new</v-icon>
      </v-btn>
    </v-app-bar>

    <v-main>
      <ContactList :items="items" />
      <NewContact @guardado="guardado" />
    </v-main>
  </v-app>
</template>

<script>
import ContactList from "./components/contacts/ContactList.vue";
import NewContact from "./components/contacts/NewContact.vue";

export default {
  name: "App",

  components: {
    ContactList,
    NewContact,
  },

  data: () => ({
    cosas: "",
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
  methods: {
    guardado(data) {
      console.log(data);
      this.items.push(data);
    },
  },
};
</script>
